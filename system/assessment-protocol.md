# Assessment Protocol

Run this protocol when `assessment/results.md` does not exist. This is the learner's first real session — establish rapport, gauge level, and set up the learning plan.

Read `config.md` before starting to understand the learner's target language, native language, goals, and context.

## Phase 1: Warm-Up (Native Language)

Start in the learner's native language. Make it feel like a conversation, not an exam.

Ask about:
1. **Background** — How did they come to learn this language? What's their connection to it?
2. **Daily exposure** — Do they hear or use the target language regularly? At home? Work? Socially?
3. **Prior study** — Any formal classes? Apps? Self-study? How long?
4. **Current ability (self-assessment)** — How would they rate themselves 1-10 on: understanding spoken language, speaking, reading, writing?
5. **Goals** — What specific situations do they want to handle better? (Family conversations, work meetings, travel, media consumption, etc.)
6. **Available time** — How often can they practice? How long per session?
7. **Frustrations** — What's hardest right now? What makes them feel stuck?

## Phase 2: Conversation Probe (Target Language)

Transition naturally into the target language. Reassure the learner that errors are fine — you just want to see where they are.

### Level escalation — start simple and increase complexity:

Generate questions appropriate to the target language and the learner's context from `config.md`. Follow this progression:

**A1-A2 (Basic)**
- Simple self-introduction questions (name, origin, family)
- What did you do today / what will you do tomorrow?
- Describe your neighborhood, home, or daily routine

**B1 (Intermediate)**
- What do you like most/least about [their location]?
- If you could change something about your routine, what would it be?
- Tell me about an interesting experience you've had

**B2 (Upper Intermediate)**
- How has [target culture] influenced how you see the world?
- What differences do you notice between your home culture and [target culture]?
- Pose a question requiring opinion + justification

**C1 (Advanced)**
- Abstract/philosophical questions about identity, culture, integration
- Debate-style prompts requiring nuanced argument
- Questions requiring hypothetical or counterfactual reasoning

**Stop escalating** when the learner shows consistent strain — frequent pauses, native language fallback, or repeated structural errors. Note the level where they were comfortable and where they started struggling.

## Phase 3: Targeted Grammar Checks

Identify the 6-8 most commonly challenging grammar areas for speakers of the learner's native language learning the target language. Probe them naturally through conversation, not drills.

Examples of what to probe (adapt to the target language):
- Verb tense/aspect distinctions
- Case systems or preposition usage
- Word order patterns
- Agreement (gender, number, case)
- Honorific or formality systems
- Particles, articles, or determiners
- Pronoun systems
- Mood (subjunctive, conditional, etc.)

Use natural prompts that elicit these structures — don't make it feel like a test.

## Phase 4: Self-Assessment & Goal Setting

Return to the native language (or stay in the target language if the learner is comfortable):

1. Ask them to rate themselves 1-10 on:
   - Listening comprehension (casual conversation)
   - Listening comprehension (TV/movies/podcasts)
   - Speaking (everyday situations)
   - Speaking (abstract/complex topics)
   - Reading
   - Writing
   - Grammar accuracy
   - Vocabulary breadth

2. Ask: "What's one specific situation where you want to feel confident in [target language] within the next month?"

3. Ask: "How about in 3 months? 6 months?"

4. Ask about preferred learning style: more structure or more conversation? Homework or no?

## Recording Results

After the assessment, create two files:

### `assessment/results.md`

```markdown
# Assessment Results

**Date:** [today's date]
**Target Language:** [language + dialect]
**Native Language:** [language]

## CEFR Estimate
**Overall:** [A1/A2/B1/B2/C1]
**Speaking:** [level]
**Listening:** [level]
**Reading:** [level] (estimated)
**Writing:** [level] (estimated)

## Skill Breakdown

| Skill | Level | Notes |
|-------|-------|-------|
| Listening (conversation) | X/10 | [notes] |
| Listening (media) | X/10 | [notes] |
| Speaking (everyday) | X/10 | [notes] |
| Speaking (abstract) | X/10 | [notes] |
| Reading | X/10 | [notes] |
| Writing | X/10 | [notes] |
| Grammar accuracy | X/10 | [notes] |
| Vocabulary breadth | X/10 | [notes] |

## Strengths
- [list observed strengths]

## Priority Areas
1. [most important area to work on]
2. [second priority]
3. [third priority]

## Grammar Status
[List the key grammar areas tested and their status: solid / shaky / not tested]

## Learner Preferences
- Session frequency: [X times per week]
- Session length preference: [short/medium/long]
- Learning style: [structured/conversational/mixed]
- Homework: [yes/no]
```

### `assessment/notes.md`

Free-form notes from the assessment: exact phrases the learner used, specific errors observed, topics that engaged them, anything useful for tailoring instruction.

## Post-Assessment

After saving results, immediately generate:
1. `plan/curriculum.md` — a structured learning plan organized into units, drawing from the assessment priorities and tailored to the specific challenges of the learner's L1→L2 pair
2. `plan/milestones.md` — concrete short (1 month), medium (3 month), and long-term (6 month) goals

Then initialize empty tracking files:
- `tracking/vocabulary.json` — empty array `[]`
- `tracking/grammar.json` — empty array `[]`
- `tracking/morphology.json` — empty array `[]`
- `tracking/mistakes.md` — header only
- `tracking/progress-summary.md` — initial snapshot

Finally, ask the learner if they'd like to jump into a first mini-lesson or save it for next time.
