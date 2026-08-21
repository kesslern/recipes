# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A personal collection of cooking recipes stored as Markdown files. There is no build, test, or lint tooling — the only "operations" are adding, editing, and organizing recipe files. The primary task is converting a source recipe (a URL, pasted text, or a photo) into a Markdown file that follows the house format.

## Recipe format

`prompt.md` defines the canonical format. Every recipe follows it:

```markdown
# Title of Recipe

## Ingredients
Bulleted ingredient list

## Instructions
Numbered step-by-step instructions

## Notes
Optional section with notes / tips
```

Additional conventions observed across the collection:

- **Source attribution goes at the bottom** as a Markdown link, e.g. `[Original Source](https://…)`. Add a `[Video Recipe](…)` link too when one exists.
- Longer recipes may include an intro blurb paragraph and a metadata block under the title (`**Prep Time:**`, `**Cook Time:**`, `**Total Time:**`, `**Servings:**`), with a `---` rule separating sections. Keep these when the source provides them; omit for simple recipes.
- Ingredients may be split into labeled sub-groups with `###` headings (e.g. `### Bread` / `### Soup`) when the recipe has distinct components.
- Use proper fraction glyphs (½, ¾, ⅓) or plain fractions (1/2) — match whatever reads cleanly; existing files use both.

## Organization

Recipes are filed into category directories, chosen by the dish's role/diet:

- `breakfast/`, `snacks/`, `sides/`, `condiments/`, `meat/`
- `vegetarian/` — meatless mains
- `veggie and meat/` — dishes with a meat and a vegetarian variant
- `components/` — sub-recipes used inside other recipes (sauces, seasonings, e.g. taco seasoning, stir-fry sauce)

Filenames are `kebab-case.md` derived from the dish name. When adding a recipe, place it in the directory matching its role and follow the existing naming.

`.gitignore` excludes `*.pdf` (source PDFs are kept locally, not committed).
