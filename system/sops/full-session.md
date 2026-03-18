# Full Session SOP

A complete lesson covering review, new material, and conversation practice. Target duration: ~30-40 minutes of interaction.

## Pre-Session (Silent)

Do this before saying anything to the learner:

1. Read `config.md` for learner context and target language
2. Read `tracking/progress-summary.md` for current state
3. Read `tracking/vocabulary.json` — identify items due for review (see `system/spaced-repetition.md` for due date calculation)
4. Read `tracking/grammar.json` — check current mastery levels
5. Read `tracking/morphology.json` — check morphology progress
6. Read `tracking/mistakes.md` — note active error patterns to watch for
7. Read `plan/curriculum.md` — identify the next topic/unit to teach
8. Read the most recent file in `sessions/` — check what was covered last time, any homework assigned
9. Prepare a mental plan: which review items, what new material, what conversation topic

## 1. Opening (~5 min)

- Greet the learner warmly in the target language
- Have a brief natural conversation to warm up
- Weave in 2-3 recently learned vocabulary items naturally in your questions/comments
- If homework was assigned last session, ask about it casually
- Note any errors for later — do NOT correct during warm-up (just recast naturally)

## 2. Review Block (~10 min)

- Select 5-8 due items from vocabulary, grammar, and morphology (prioritize per spaced-repetition.md)
- Present items using varied formats (see spaced-repetition.md "Review Formats")
- For each item, note the result:
  - Correct + no hesitation → promote
  - Correct + hesitation → flat
  - Incorrect or couldn't recall → demote
- If the learner gets something wrong, don't just give the answer — guide them:
  - Give a hint or context clue first
  - If still stuck, give the answer in a natural sentence
  - If it's a grammar item, briefly explain the pattern
- Keep the energy up — this should feel like a game, not an exam
- Transition naturally to new material in the target language

## 3. New Material (~10 min)

- Introduce the next topic from `plan/curriculum.md`
- **For vocabulary:**
  - Present 3-5 new words in context (not isolated word lists)
  - Give each word in a natural example sentence relevant to the learner's life (from `config.md`)
  - Include any dialect-appropriate vocabulary
  - Ask the learner to create their own sentence with each new word
- **For grammar:**
  - Introduce max 1 new grammar concept
  - Start with examples, then explain the pattern (inductive approach)
  - Give 3-5 example sentences showing the pattern
  - Contrast with the learner's native language if helpful (but don't over-rely on translation)
  - Have the learner practice with 2-3 guided examples
- **For morphology (conjugations, declensions, etc.):**
  - Present the pattern with a familiar word first
  - Show 2-3 more words following the same pattern
  - Practice with fill-in-the-blank or translation
  - For analytic languages (e.g., Mandarin), focus on word order, particles, or measure words instead
- Connect new material to previously learned items when possible

## 4. Conversation Practice (~15 min)

This is the most important part. The learner needs to USE the language.

- Choose one of these formats based on what was taught:
  - **Cultural scenario**: Role-play a real situation from the learner's daily life (from `config.md` — local interactions, social situations, errands, family gatherings, etc.)
  - **Abstract discussion**: Pose a philosophical or opinion question using target structures (great for subjunctive, conditional, discourse markers, opinion structures)
  - **Storytelling**: Ask the learner to tell a story about something that happened to them (great for tense/aspect practice)
  - **Debate**: Take opposing sides on a topic the learner cares about (great for argument structures)

- During conversation:
  - Let the learner speak — don't dominate
  - Use recasting for errors (repeat what they said correctly without breaking flow)
  - Naturally use the new vocabulary/grammar from today's lesson
  - Push them to use new structures: encourage rephrasing with the target structure
  - If they fall back to their native language for a word, provide the target language word and have them re-say the sentence
  - Track errors mentally for the mistakes log

## 5. Wrap-Up (~5 min)

- Summarize what was covered today (in the target language, keep it brief)
- Highlight 1-2 things the learner did well
- Mention 1 thing to focus on
- Optional homework — keep it light and practical:
  - "Try using [word] in conversation this week"
  - "Next time you're at [local place], try [structure]"
  - "Think about how you'd answer: [question in target language]"
- Close warmly in the target language

## Post-Session (Silent)

Update all tracking files — this is mandatory, do not skip:

### Update `tracking/vocabulary.json`
- Add any new vocabulary items introduced today with initial metadata:
  - `confidence: 1`, `review_interval_days: 1`, `last_reviewed: null`, `times_reviewed: 0`, `times_correct: 0`, `status: "active"`
- Update reviewed items: new confidence, new interval, new `last_reviewed` date, increment counters

### Update `tracking/grammar.json`
- Add any new grammar concepts introduced
- Update mastery levels for practiced concepts
- Add any common errors observed

### Update `tracking/morphology.json`
- Add any new morphological patterns practiced (conjugations, declensions, measure words, etc.)
- Update mastery levels

### Update `tracking/mistakes.md`
- Add any new error patterns observed
- Update frequency/date for recurring patterns
- Mark any resolved patterns

### Update `tracking/progress-summary.md`
- Update last_session date, increment total_sessions
- Update current unit/lesson
- Refresh items due counts
- Update streak if applicable

### Create `sessions/YYYY-MM-DD.md`
Create a session log with:
- YAML frontmatter: date, session_number, session_type (full-session), curriculum_lesson
- Topics covered
- Review results table (item, format, result, new confidence)
- New vocabulary/grammar introduced
- Conversation notes (topic, how it went, notable usage)
- Errors observed
- Homework assigned
- Brief assessment notes (overall impression, what to focus on next)
