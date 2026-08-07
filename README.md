# Battery & Energy Storage Literature

A curated, browsable catalog of battery safety and energy storage research literature —
built to make it faster to find and compare papers by chemistry, topic, and study type.

**Live site:** https://dhevkannan.com/energystorage-literature/

## What's in this repo

This repo holds only the static, generated website — not the pipeline that produces it.

```
docs/
  index.html     the public catalog — browse by chemistry/tag, click through to each
                 paper's DOI. No abstracts or extracted text shown here.
  papers.json    the data behind both pages, generated from a private local pipeline
```

`index.html` is a single self-contained page — no build step, no framework, no
dependencies. It fetches `papers.json` and renders everything client-side.

## How the data gets here

Papers are collected, deduplicated, and classified locally (chemistry, study type,
reliability, tags) against OpenAlex/Crossref/Semantic Scholar, then exported to
`papers.json` and pushed here. That pipeline — and a second, private view with
abstracts and extracted methodology for personal reading/note-taking — isn't part of
this public repo.

## Why DOI links, not hosted PDFs

The catalog links out to each paper's DOI rather than hosting any full text. Most
entries are copyrighted journal articles under institutional access — linking to the
canonical source respects that, and a DOI link is more durable than a copied file
anyway.

## Tech

Plain HTML/CSS/JS, hosted on GitHub Pages. No build tooling, no package manager, no
server — the entire site is `index.html` + `papers.json`.

## License / usage

This is a personal research tool shared for reference. The code here (`index.html`)
is free to reuse or adapt. `papers.json` reflects bibliographic metadata (titles,
authors, DOIs, categorization) about third-party publications — not the underlying
papers themselves, which remain the property of their respective publishers.
