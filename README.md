# Tongue

A CLAUDE.md boot script that turns [Claude Code](https://docs.anthropic.com/en/docs/claude-code) into a stateful language tutor with spaced repetition, adaptive curriculum, and progress tracking.

## What it does

When you open this project in Claude Code and start chatting, the boot script takes over. Claude becomes a patient, encouraging language tutor that:

- **Adapts to any language** — Spanish, Japanese, Arabic, Mandarin, French, Russian, or anything else
- **Tracks your progress** with spaced repetition across vocabulary, grammar, and morphology
- **Remembers between sessions** — picks up where you left off, reviews what's due, advances the curriculum
- **Teaches naturally** — conversation-first approach with error correction via recasting, not interruption
- **Grounds examples in your life** — uses your location, cultural context, and goals to make lessons relevant

## Quick start

1. Clone this repo
2. Open the directory in [Claude Code](https://docs.anthropic.com/en/docs/claude-code)
3. Start chatting

On first launch, the tutor will walk you through:
1. **Configuration** — your target language, dialect, goals, and preferences
2. **Terminal setup** — keyboard/input method for typing in your target language
3. **Assessment** — a conversational evaluation to gauge your current level
4. **Curriculum** — a personalized learning plan based on your assessment

After that, each session picks up where you left off.

## Session types

| Session | Duration | Best for |
|---------|----------|----------|
| **Full session** | ~30-40 min | Review + new material + conversation practice |
| **Quick review** | ~10 min | Spaced repetition of due items |
| **New concept** | ~15 min | Focused intro of one grammar or vocabulary topic |

The tutor suggests a session type based on your current state — quick review if items are overdue, new concept if you're caught up, full session as the default.

## How tracking works

All progress is tracked in JSON files and updated after every session:

- **Vocabulary** — words and phrases with confidence levels (1-5), review intervals, and usage examples
- **Grammar** — concepts with mastery levels, practice history, and common errors
- **Morphology** — conjugations, declensions, measure words, or other language-specific patterns
- **Mistakes** — recurring error patterns, tracked over time to monitor improvement
- **Progress summary** — snapshot of where you are in the curriculum

The spaced repetition system uses a confidence-to-interval mapping (1 day → 2 → 4 → 8 → 16 days) with promotion, flat, and demotion based on recall quality.

## Project structure

```
tongue/
├── CLAUDE.md                    # Boot script — the core of the tutor
├── config.md                    # Your language/goals/preferences (generated)
├── system/
│   ├── config-protocol.md       # Interactive setup protocol
│   ├── terminal-setup.md        # Keyboard/input method guide
│   ├── tutor-persona.md         # Teaching style and adaptation rules
│   ├── assessment-protocol.md   # Initial level assessment
│   ├── spaced-repetition.md     # SRS rules and intervals
│   └── sops/
│       ├── full-session.md      # Full lesson protocol
│       ├── rapid-review.md      # Quick review protocol
│       └── new-concept.md       # New concept protocol
├── assessment/                  # Assessment results (generated)
├── plan/                        # Curriculum and milestones (generated)
├── tracking/                    # Progress data (generated)
│   ├── README.md                # JSON schemas for tracking files
│   ├── vocabulary.json
│   ├── grammar.json
│   ├── morphology.json
│   ├── mistakes.md
│   └── progress-summary.md
├── sessions/                    # Session logs (generated)
└── practice/                    # Reference materials (generated)
    └── README.md
```

Files marked "(generated)" are created by the tutor during sessions and are gitignored.

## Language support

Tongue works with any language. The system files are language-agnostic — all language-specific behavior is driven by your `config.md`. The tutor adapts its approach based on the target language:

- **Latin-script languages** (Spanish, French, German, etc.) — accent handling, dialect vocabulary
- **CJK languages** (Chinese, Japanese, Korean) — IME setup, script learning, tonal practice
- **RTL languages** (Arabic, Hebrew, Persian) — keyboard setup, script direction
- **Cyrillic/other scripts** (Russian, Hindi, Thai, etc.) — keyboard layouts, script introduction
- **Highly inflected languages** (Russian, German, Latin, etc.) — morphology tracking for cases/declensions
- **Analytic languages** (Mandarin, Vietnamese, Thai) — tone, particle, and word-order focus

## Requirements

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) CLI
