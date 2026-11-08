---
layout: student-project
permalink: /projects/document-search/
title: "Search your documents. Show the evidence."
description: "Build a small document search tool, compare lexical and semantic retrieval, and test whether answers are supported by their sources."
project_fit: "A first independent project; Python, basic ML, and an interest in making something useful."
project_resources: "An ordinary laptop and a small collection you may use. No GPU or paid API is needed for the core project."
---

Build a tool that answers questions about a small collection: a club handbook, your own course notes, or public documentation for a student activity. Every result should take the reader to the supporting passage. If the collection does not contain an answer, the tool should make that clear.

The interesting question is whether a more elaborate system actually helps someone find reliable information. Start with search and quotations. Generated answers are an optional addition once that works.

## First session: find one useful passage

Choose five short text documents that you wrote or have permission to use. Prefer clean text over scanned PDFs initially. Split them at headings or paragraphs, preserving a document ID and location. Use scikit-learn's `TfidfVectorizer` and cosine similarity to show the three highest-scoring passages for a query.

Try five questions whose answers you can locate yourself. Save the query, retrieved passage IDs, and scores. You have a first result when a friend can ask a question and follow a result back to the source.

**Check before proceeding:** Does the displayed text exactly match the source? Are headings and page or section references preserved? Fix extraction problems before adding a language model.

## Milestone 1: make a small evaluation set

Expand to roughly 10–20 documents. Write 40 questions: about 25 answerable from the collection, 10 absent from it, and five involving an outdated or conflicting statement. Record the expected answer, supporting passage IDs, and why a question cannot be answered when appropriate. A useful row has `question_id`, `question`, `status`, `evidence_ids`, `expected_answer`, and `split`.

Reserve half for development and half for the final check, with each category represented. Keep questions about the same underlying fact in the same split. Ask another reader to verify a sample of your references. These counts make a manageable pilot; they are not enough for claims about all document collections.

**Deliverable:** a versioned document inventory and a checked question file. If a question's answer is disputed, fix the label or record the disagreement.

## Milestone 2: compare two retrieval methods

Keep TF–IDF as your baseline. Add a small sentence-embedding model and search by vector similarity. Use the same passages and questions so the comparison is fair. Tune chunk size or retrieval settings only on the development questions.

On answerable questions, report **evidence hit rate at three**: the fraction for which the first three results include a supporting passage. If an answer needs two passages, also check whether both are retrieved. Record query latency and inspect at least ten failures. Check names, abbreviations, exact course codes, and paraphrases; different methods may help different queries.

**Check before proceeding:** A higher similarity score is not proof that a passage answers the question. If semantic search loses to TF–IDF, investigate and report that. It is a useful outcome.

## Milestone 3: handle missing and conflicting evidence

Show source dates and flag known conflicts in your collection. On development data, try a simple threshold for saying “I could not find enough evidence.” For the quotation-only tool, count a query as answered when it presents a passage as supporting evidence, and as declined when it explicitly says there is insufficient evidence. Evaluate on held-out questions. Report both **unsupported questions answered anyway** and **answerable questions declined**; a system that declines everything is not useful.

If you add generated answers, give the model only the retrieved passages and require source references. Audit every factual claim in the small held-out set: does the cited passage support it? Compare against simply showing quotations. Treat document text as evidence, never as instructions to the system. Include a test passage saying “ignore the question” and verify that it cannot change the tool's behaviour.

**Human judgement:** You decide what the documents support, whether a date matters, and whether two sources genuinely conflict. An AI judge can suggest problems, but should not be the sole grader of another model's answers.

## A solid stopping point

A small local interface, a reproducible comparison of two retrieval methods, an evaluation of missing evidence, and a short account of failures. Include examples where the simpler method wins. Keep official documents linked and dated; label the tool as a student prototype rather than an authoritative source for college decisions.

This is already a complete project without answer generation. If you add it, report citation correctness separately from retrieval quality.

## Choose one extension

- Add questions in a language you know and compare retrieval across languages.
- Replace a source with an updated version and measure which answers become stale.
- Add tables or scanned pages and measure whether extraction, retrieval, or answering becomes the main failure.

## Starting resources

- [scikit-learn: text feature extraction](https://scikit-learn.org/stable/modules/feature_extraction.html#text-feature-extraction) for the TF–IDF baseline.
- [Sentence Transformers: semantic search](https://www.sbert.net/examples/sentence_transformer/applications/semantic-search/README.html) for the embedding comparison.

Use a small collection you can inspect completely. Avoid personal student records or documents you cannot share with the tools you use.
