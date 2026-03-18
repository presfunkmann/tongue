# Tracking

This directory holds the learner's progress data, managed automatically by the tutor. All files here are generated — do not edit manually.

## File Schemas

### `vocabulary.json`

Array of vocabulary items:

```json
{
  "term": "string — the word or phrase in the target language",
  "translation": "string — meaning in the learner's native language",
  "example_sentence": "string — natural example sentence",
  "category": "string — thematic category (e.g., 'daily life', 'abstract', 'slang')",
  "tags": ["array of strings — e.g., 'formal', 'colloquial', dialect tags"],
  "confidence": "number 1-5 — current spaced repetition confidence",
  "review_interval_days": "number — days until next review",
  "last_reviewed": "string (YYYY-MM-DD) or null — date of last review",
  "times_reviewed": "number — total review count",
  "times_correct": "number — correct responses count",
  "status": "string — 'active' or 'graduated'",
  "date_introduced": "string (YYYY-MM-DD) — when the item was first taught",
  "notes": "string — additional context, common errors, usage notes"
}
```

### `grammar.json`

Array of grammar concepts:

```json
{
  "concept": "string — name of the grammar concept",
  "description": "string — brief explanation",
  "curriculum_unit": "string — which curriculum unit this belongs to",
  "mastery_level": "number 1-3 — 1=new/weak, 2=in progress, 3=solid",
  "date_introduced": "string (YYYY-MM-DD)",
  "last_practiced": "string (YYYY-MM-DD) or null",
  "sessions_practiced": "number — how many sessions have included this concept",
  "common_errors": ["array of strings — recurring mistakes related to this concept"],
  "notes": "string — additional context"
}
```

### `morphology.json`

Array of morphological patterns (conjugations, declensions, measure words, etc.):

```json
{
  "item": "string — the word, verb, or pattern",
  "type": "string — e.g., 'verb conjugation', 'noun declension', 'measure word', 'particle'",
  "pattern": "string — the morphological pattern or paradigm",
  "tense_or_form": "string — specific tense, case, or form being tracked",
  "mastery": "number 1-3 — 1=new/weak, 2=in progress, 3=solid",
  "date_introduced": "string (YYYY-MM-DD)",
  "last_practiced": "string (YYYY-MM-DD) or null",
  "sessions_practiced": "number",
  "common_errors": ["array of strings"],
  "notes": "string"
}
```

### `mistakes.md`

Markdown file documenting recurring error patterns. Each entry includes:
- Error description and category
- Status (active / improving / resolved)
- Examples (what the learner said vs. correct form)
- Date first observed and last seen
- Notes on remediation progress

### `progress-summary.md`

Markdown snapshot of overall progress:
- Current curriculum phase and unit
- Sessions completed
- CEFR estimate
- Active focus areas
- Vocabulary and grammar stats
- Recent wins and persistent challenges
