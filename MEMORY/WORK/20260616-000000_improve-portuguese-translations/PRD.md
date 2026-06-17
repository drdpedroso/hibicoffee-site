---
task: improve portuguese translations on hibi site
slug: 20260616-000000_improve-portuguese-translations
effort: standard
phase: complete
progress: 0/0
mode: interactive
started: 2026-06-16T00:00:00Z
updated: 2026-06-16T00:01:00Z
---

## Context
Hibi site (index.html) has a JS i18n object with EN/PT/ES strings. The `pt` block is the target.
Reviewed all ~40 PT strings against EN originals to identify awkward phrasing, unnatural word choices,
and places where personality from the EN copy was lost in translation.

### Risks
- Subjective — some changes are style preferences. Keep changes to clearly better phrasing only.
- Don't break the JS string syntax (quotes, escaping).

## Criteria
- [x] ISC-1: `feat2.p` uses "mesmo em segundo plano" instead of "até em segundo plano"
- [x] ISC-2: `band.p` uses "as luzes diminuem" instead of "as luzes baixam"
- [x] ISC-3: `band.li2` uses "preciso mesmo com a tela bloqueada" instead of awkward "sem atrasar quando a tela bloqueia"
- [x] ISC-4: `methods.h2` uses "Receitas que vale copiar" capturing "worth stealing" personality
- [x] ISC-5: `ethos3.p` uses "nada é supérfluo" instead of "nada é enchimento"
- [x] ISC-6: All other PT strings remain unchanged
- [x] ISC-7: JS syntax remains valid after edits
- [x] ISC-8: No EN strings accidentally modified

## Decisions

## Verification
