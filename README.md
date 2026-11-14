# Kana Academy — Incremental Stage 4 update

This version separates completed kana fundamentals from new reading-mechanics practice.

## Learning tracks

- **Kana fundamentals · review** keeps the original kana practice available as optional review. Its progress and mastery remain unchanged.
- **Stage 4 · Reading mechanics** is a focused queue containing only the 30 new small-っ and long-vowel words. It does not mix in the 416 previously mastered kana directions.

## Mastery and progress

- Each word has independent Kana → Romaji and Romaji → Kana streaks.
- Each direction requires 10 consecutive correct answers. An incorrect answer resets only that direction.
- Progress bars now show the mastery streak (0–10), not overall accuracy. They turn fully green only when that direction is mastered.
- The top-level mastered-directions total counts the full catalog, including the original 416 directions and the 60 new Stage 4 directions.

## Progress preservation

- Uses the existing localStorage key `kanaAcademy_v1`.
- Keeps existing basic kana, voiced kana, contracted-sound progress and the legacy hiragana mastery migration.
- Adds Stage 4 word progress without resetting existing records.

## Publish

1. Export a backup from Progress details before replacing files.
2. Extract this ZIP and replace the five files in the GitHub Pages publishing root.
3. Commit the changes and wait for the Pages deployment to complete.
4. Reload the published site. The service-worker cache is bumped to v6.

Progress is local to this device/browser. Keep the exported backup in a safe place.
