# New Concept SOP

Focused introduction of one new grammar or vocabulary concept. Teach it well, practice it briefly, and add it to tracking. Target duration: ~15 minutes.

## Pre-Session (Silent)

1. Read `config.md` for learner context and target language
2. Read `plan/curriculum.md` — identify the next concept to introduce
3. Read `tracking/grammar.json` — confirm it hasn't already been introduced
4. Read `tracking/vocabulary.json` — check for related vocabulary already known
5. Read `tracking/mistakes.md` — check if this concept relates to an active error pattern
6. Read the most recent session log for continuity

If the learner requests a specific concept, teach that instead of the next curriculum item.

## 1. Opening

- Brief greeting in the target language
- Tell the learner what today's focus is: name the concept and its practical application (in the target language)
- Connect it to something they already know or a situation they've encountered

## 2. Presentation (~5 min)

### For Grammar Concepts:
- Start with 3-5 **example sentences** — let the learner see the pattern before explaining it
- Ask if they notice a pattern (in the target language)
- Explain the rule/pattern clearly and concisely
- Contrast with the learner's native language if it helps understanding
- Show common mistakes and how to avoid them
- Give 2-3 more examples grounded in the learner's daily life (from `config.md`)

### For Vocabulary Sets:
- Present 3-5 thematically linked words
- Each word gets:
  - The word + pronunciation notes if needed
  - A natural example sentence (grounded in the learner's context)
  - Any common collocations or phrases
  - Register notes (formal/informal/slang)
- Point out any cognates, false cognates, or etymological connections

### For Morphology Patterns (conjugations, declensions, measure words, etc.):
- Present the pattern using a familiar word
- Show the full paradigm (but focus on the most-used forms)
- Give 2-3 example words following the same pattern
- Highlight irregularities if any
- Compare to patterns the learner already knows
- For analytic languages, focus on particles, word order, classifiers, or other relevant patterns instead

## 3. Guided Practice (~5 min)

3-4 structured exercises:

1. **Fill-in-the-blank**: Provide a sentence with the target structure missing
2. **Translation**: Give a sentence in the native language that requires the new concept
3. **Choice**: Present two options — which one is correct and why?
4. **Creation**: Ask the learner to create their own sentence using the concept

After each exercise:
- If correct: brief positive feedback + move on
- If incorrect: explain why, give another example, try a similar exercise

## 4. Mini-Scenario (~5 min)

A brief, focused conversation or role-play that naturally requires the new concept:

- Set up a realistic situation from the learner's life (from `config.md`)
- Have a 4-6 exchange conversation where the concept comes up naturally
- Gently push the learner to use the new structure
- Recast any errors naturally
- Keep it short and focused — this isn't the full conversation block

## 5. Wrap-Up

- Briefly restate the key rule/pattern in one sentence
- Give one practical "homework" challenge tied to the learner's daily life
- Preview what's coming next from the curriculum

## Post-Session (Silent)

### Update `tracking/vocabulary.json`
- Add any new vocabulary items:
  - `confidence: 1`, `review_interval_days: 1`, `last_reviewed: null` (will be reviewed in next review session)
  - `times_reviewed: 0`, `times_correct: 0`, `status: "active"`
  - Include `example_sentence`, `category`, relevant `tags`

### Update `tracking/grammar.json`
- Add the new concept:
  - `mastery_level: 1` (just introduced)
  - `date_introduced: today`
  - `sessions_practiced: 1`
  - Include `description`, `curriculum_unit`
  - Add any errors observed to `common_errors[]`

### Update `tracking/morphology.json`
- If a new morphological pattern was introduced, add it with initial mastery

### Update `tracking/mistakes.md`
- Log any errors observed during practice

### Update `tracking/progress-summary.md`
- Update last_session, increment total_sessions
- Update current unit/lesson to reflect the new concept
- Note what was introduced

### Create `sessions/YYYY-MM-DD.md`
Session log:
- YAML frontmatter: date, session_number, session_type (new-concept), curriculum_lesson
- Concept introduced: name + brief description
- Examples used
- Practice results
- Errors observed
- Conversation notes from mini-scenario
- Homework assigned
