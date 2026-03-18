# Terminal Setup Guide

Run this once, right after config setup, before the first assessment. The goal is to make sure the learner can type in their target language within the terminal.

## Detect Environment

Check the OS from the system environment (macOS, Linux, or Windows/WSL). Tailor instructions accordingly.

## Language Categories

### Latin-Script Languages with Diacritics
*Spanish, French, German, Portuguese, Vietnamese, Turkish, Polish, Czech, etc.*

**macOS:**
- The default keyboard can produce most accents with Option key combinations:
  - `Option + e`, then vowel → acute accent (é, á, ó, ú, í)
  - `Option + u`, then vowel → umlaut (ü, ö, ä)
  - `Option + n`, then n → ñ
  - `Option + i`, then vowel → circumflex (ê, â, ô)
  - `Option + c` → ç
  - `Option + 1` → ¡ / `Option + ?` → ¿ (Spanish)
- Alternative: Add the target language keyboard in System Settings → Keyboard → Input Sources. Switch with `Ctrl + Space` or Globe key.

**Linux:**
- Compose key method: Set a compose key in keyboard settings, then use sequences (e.g., Compose + `'` + `e` → é)
- Or add the language keyboard layout and switch with `Super + Space`
- For GNOME: Settings → Keyboard → Input Sources → Add

**Windows/WSL:**
- Settings → Time & Language → Language & Region → Add a language
- Switch with `Win + Space`
- US International keyboard layout supports dead keys for accents

### CJK Languages (Chinese, Japanese, Korean)

**macOS:**
- System Settings → Keyboard → Input Sources → Add:
  - Chinese: "Pinyin - Simplified" or "Pinyin - Traditional" (or Zhuyin/Cangjie)
  - Japanese: "Hiragana" (includes katakana and kanji conversion)
  - Korean: "2-Set Korean"
- Switch input with `Ctrl + Space` or Globe key
- In terminal: most modern terminals (iTerm2, Terminal.app, Kitty, Wezterm) support IME input natively

**Linux:**
- Install an IME framework: `fcitx5` or `ibus`
- Chinese: `fcitx5-chinese-addons` (Pinyin) or `ibus-libpinyin`
- Japanese: `fcitx5-mozc` or `ibus-mozc`
- Korean: `fcitx5-hangul` or `ibus-hangul`
- Configure and restart. Switch with the configured hotkey.

**Windows/WSL:**
- Add the language via Settings → Time & Language
- Microsoft IME is built-in for Chinese, Japanese, Korean
- In WSL terminal: depends on the terminal app (Windows Terminal supports IME)

### RTL Languages (Arabic, Hebrew, Persian, Urdu)

**macOS/Linux/Windows:**
- Add the language keyboard layout as above
- **Terminal considerations:** Most terminals render RTL text left-to-right. This is a known limitation.
  - The learner should know: text entry works fine, but display may look odd
  - For practice, the tutor will handle RTL display context
  - Dedicated terminal emulators with better bidi support: mlterm, or use a text editor alongside

### Cyrillic-Script Languages (Russian, Ukrainian, Bulgarian, Serbian, etc.)

**macOS:**
- System Settings → Keyboard → Input Sources → Add "Russian" (or target language)
- Switch with `Ctrl + Space`
- Tip: "Russian - Phonetic" layout maps sounds to similar Latin keys (e.g., pressing `d` types `д`)

**Linux:**
- Add via keyboard settings or `setxkbmap ru phonetic`
- Switch with configured hotkey

**Windows:**
- Add via Language settings. Mnemonic layout available for Russian.

### Other Scripts (Devanagari, Thai, Greek, Georgian, Armenian, etc.)

- Follow the same pattern: add the keyboard layout through OS settings
- For complex scripts (Thai, Devanagari), the OS built-in keyboards work well
- Recommend phonetic/transliteration layouts where available for beginners

## Verification

After walking through setup, verify it works:

1. Ask the learner to type 3-5 characters specific to the target language
   - Spanish: "Try typing: ¿Cómo estás? — you'll need ¿ and the accent on á"
   - Japanese: "Try typing: こんにちは — type 'konnichiha' and select the hiragana"
   - Russian: "Try typing: Привет — that's 'privet' on a phonetic keyboard"
   - Arabic: "Try typing: مرحبا — that's 'mrhba' on the Arabic keyboard"
   - Adapt examples to whatever the target language is

2. If it works → "You're all set! Let's move on to the assessment."
3. If it doesn't work → troubleshoot. Common issues:
   - IME not activated in terminal (restart terminal)
   - Wrong keyboard layout selected
   - Terminal doesn't support the script (suggest alternative terminal)

## Notes

- Keep this practical and encouraging — don't overwhelm with options
- If the learner says they already have input set up, verify quickly and move on
- For languages that use the Latin alphabet without diacritics (e.g., Malay, Indonesian), skip this step entirely and note that no special setup is needed
