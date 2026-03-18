# Spaced Repetition System

## Confidence-to-Interval Mapping

| Confidence | Interval | Meaning |
|------------|----------|---------|
| 1 | 1 day | New or very shaky — review tomorrow |
| 2 | 2 days | Recognized but not solid |
| 3 | 4 days | Getting comfortable, some hesitation |
| 4 | 8 days | Solid, minor hesitation only |
| 5 | 16 days | Strong — nearly automatic |

## When an Item Is Due

An item is due for review when:

```
today >= last_reviewed + review_interval_days
```

If `last_reviewed` is `null` (never reviewed), the item is due immediately.

## Updating Confidence After Review

### Promotion (confidence + 1, max 5)
- The learner produces the item **correctly** with **no hesitation**
- Applies to: translation, fill-in-blank, free usage in conversation

### Flat (confidence stays the same)
- The learner produces the item **correctly** but with **noticeable hesitation** or self-correction
- This means it's not yet automatic — keep at the same interval

### Demotion (confidence - 1, min 1)
- The learner produces the item **incorrectly** or **cannot recall** it
- Also demote if the learner uses native language fallback for an item they've been taught

## After Updating Confidence

1. Set `review_interval_days` to the new interval from the table above
2. Set `last_reviewed` to today's date
3. Increment `times_reviewed` by 1
4. If correct, increment `times_correct` by 1

## Review Priority Order

When multiple items are due, present them in this order:

1. **Weakest first** — lowest confidence items
2. **Most overdue** — items where `(today - last_reviewed)` most exceeds `review_interval_days`
3. **Thematically related** — items related to today's lesson topic (to reinforce connections)

## Graduation

An item **graduates** from active review when:
- Confidence = 5
- Has been reviewed at confidence 5 at least **3 times**
- Set `status` to `"graduated"`

Graduated items are not included in review queues.

## Re-Introduction

If a graduated item is used **incorrectly** during free conversation or practice:
- Set `status` back to `"active"`
- Set `confidence` to 3
- Set `review_interval_days` to 4
- Note in the item's `notes` field: "Re-introduced [date] — used incorrectly in conversation"

## Review Formats

Vary the format to test different retrieval paths:

1. **Native → Target translation**: "How do you say '[word]' in [target language]?"
2. **Target → Native**: "What does '[word]' mean?"
3. **Fill-in-the-blank**: Provide a sentence with the target item missing
4. **Contextual usage**: "How would you say [scenario] using [target word/structure]?"
5. **Morphology check** (conjugation, declension, measure words, etc.): "How would you say '[phrase]' in [target language]?"
6. **Error correction**: "Is this correct? '[sentence with error]'"

Use formats 1-3 for confidence 1-2 items. Use formats 4-6 for confidence 3+ items.

## Per-Session Limits

- **Quick review**: up to 15 due items
- **Full session review block**: 5-8 due items
- If more items are due than the limit, prioritize by the order above and carry the rest to next session
