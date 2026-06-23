# Eva Petitdemange, academic website (Quarto)

## What this is

A Quarto website project: 4 pages (Home, CV, Publications, Contact). Publications are generated automatically from `references.bib`, you never edit the Publications page directly, you edit the .bib file.

Everything marked `[À COMPLÉTER]`, `PLACEHOLDER`, or `[À VALIDER]` is not real content. I did not invent biography, dates, or publications, those need to come from you.

## One time setup

1. Install Quarto: https://quarto.org/docs/get-started/ (pick your OS, it's a single installer, no separate Hugo/Go install needed).
2. Open a terminal in this folder.

## Preview while editing

```
quarto preview
```

This opens the site in your browser and re-renders automatically every time you save a file. Leave it running while you edit.

## Before going live, replace

- `profile.jpg`: your photo (square, 400px or larger), still missing
- `index.qmd`: TL;DR line, news items dates, confirm research interests list
- `cv.qmd`: confirm current title/HDR status, the recent-projects list, networks list (all marked À VALIDER)
- `contact.qmd`: add LinkedIn if wanted, confirm CGI/IMT page URL
- `references.bib`: 27 of an estimated 30 HAL entries. Export BibTeX directly from your HAL CV when you can to get the last few and to fix any transcription errors on my part
- `_quarto.yml`: site-url, footer year, LinkedIn link

## Publish

Two options, pick one:

**GitHub Pages** (free, needs a GitHub account and basic git familiarity):
```
quarto publish gh-pages
```
This builds the site and pushes it to a `gh-pages` branch for you. Quarto will ask you to confirm a GitHub login the first time.

**Any other host (including an IMT Mines Albi server)**:
```
quarto render
```
This builds a static `_site/` folder. Upload the contents of `_site/` to your host via whatever method they require (FTP, SCP, a web upload form). No further build step needed on the server side, since it's plain HTML/CSS at that point.

## Adding a new publication later

Add an entry to `references.bib` in standard BibTeX format, save, re-render (`quarto preview` or `quarto render`). That's the entire workflow, no HTML editing.
