---
task: Screenshot PT page sections for copy review
slug: 20260616-000001_screenshot-pt-page-sections-copy-review
effort: standard
phase: complete
progress: 11/11
mode: interactive
started: 2026-06-16T00:00:01Z
updated: 2026-06-16T00:00:04Z
---

## Context

User wants to QA the Brazilian Portuguese localization of the Hibi site at `http://localhost:8743/index.html`. The task is to open the page in a browser, click the PT language switcher button in the top nav, then capture screenshots of 6 named sections in order. After screenshots, analyze whether the copy reads naturally in Brazilian PT, and flag any awkward phrasing, truncation, or layout misalignment.

### Risks
- Dev server may not be running on port 8743
- Language switcher may not be labeled exactly "PT" (could be a flag or different text)
- Some sections may require scrolling to reach
- Screenshot quality must be sufficient to read copy

## Criteria

- [x] ISC-1: Browser opens to http://localhost:8743/index.html successfully
- [x] ISC-2: PT language switcher button located in top nav
- [x] ISC-3: PT button clicked and page switches to Portuguese
- [x] ISC-4: Hero section screenshot captured showing headline and subtext
- [x] ISC-5: Features section screenshot captured ("O ritual" / "Tudo o que você precisa")
- [x] ISC-6: Brewing mode band screenshot captured ("Modo preparo" / "Despejos guiados")
- [x] ISC-7: Methods section screenshot captured ("A biblioteca" / "Cinco métodos")
- [x] ISC-8: Ethos/"Por que Hibi" section screenshot captured
- [x] ISC-9: Footer screenshot captured
- [x] ISC-10: Copy analysis provided: natural Brazilian PT assessment for each section
- [x] ISC-11: Awkward, truncated, or misaligned text flagged specifically

## Decisions

## Verification
