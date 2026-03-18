# Rapid Review SOP

A focused spaced-repetition review session for items that are due. Quick and efficient. Target duration: ~10 minutes.

## Pre-Session (Silent)

1. Read `config.md` for learner context and target language
2. Read `tracking/vocabulary.json` — compute all due items
3. Read `tracking/grammar.json` — check for grammar concepts due for review
4. Read `tracking/morphology.json` — check for morphology items due
5. Read `tracking/mistakes.md` — note active patterns (may inform review emphasis)
6. Read `system/spaced-repetition.md` — refresh on rules

Count total due items. If more than 15, select the top 15 by priority (weakest → most overdue → thematically related).

If nothing is due, tell the learner and suggest a different session type instead.

## 1. Opening

- Brief greeting in the target language
- Tell the learner how many items are up for review (in the target language)
- Jump straight in — no warm-up conversation needed

## 2. Review

Present each due item using varied formats (see `system/spaced-repetition.md` "Review Formats"):

- Use simpler formats (translation, definition) for low-confidence items (1-2)
- Use contextual formats (usage, error correction) for higher-confidence items (3+)
- Mix vocabulary, grammar, and morphology items — don't cluster by type
- Keep a brisk pace — this is about recall, not deep practice

For each item, record:
- **Result**: correct (no hesitation) / correct (with hesitation) / incorrect
- **New confidence**: promote / flat / demote per spaced-repetition rules

If the learner misses an item:
- Give a brief hint or context clue
- If still stuck, provide the answer in a natural sentence
- Move on — don't dwell (this isn't a teaching session)

After every 5 items, give a quick status update in the target language.

## 3. Wrap-Up

- Quick summary in the target language: how many reviewed, how many correct, how many need more practice
- Highlight items that improved (promoted)
- Note items that dropped
- If many items were missed, suggest a full session to review those topics
- Brief close in the target language

## Post-Session (Silent)

### Update `tracking/vocabulary.json`
- For each reviewed vocab item: update confidence, review_interval_days, last_reviewed (today), increment times_reviewed, increment times_correct if correct

### Update `tracking/grammar.json`
- For each reviewed grammar concept: update mastery_level, last_practiced

### Update `tracking/morphology.json`
- For each reviewed morphology item: update mastery, last_practiced

### Update `tracking/progress-summary.md`
- Update last_session date
- Increment total_sessions
- Refresh due item counts
- Update streak

### Create `sessions/YYYY-MM-DD.md`
Short session log:
- YAML frontmatter: date, session_number, session_type (rapid-review)
- Review results table: item | format | result | old confidence → new confidence
- Summary: total reviewed, total correct, total promoted, total demoted
- Items that need extra attention
