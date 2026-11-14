# Kana Academy — Stage 5: First Kanji & Vocabulary

This update adds a separate Stage 5 learning track while preserving the existing `kanaAcademy_v1` local save data.

## Stage 5 content
- Introduces 10 beginner kanji: 山, 川, 日, 月, 人, 大, 小, 水, 火, 木.
- Starts with 11 focused vocabulary items, including 火山. Each item includes its Japanese form, kana reading, romaji support, and one clear English meaning.
- Includes a Kanji guide with core meaning and common on-yomi / kun-yomi reading patterns. These are introductory common readings, not an exhaustive dictionary.
- Practice directions: Japanese → English and English → Japanese, including random direction.
- Each vocabulary item tracks mastery independently in both directions. Mastery requires 10 consecutive correct answers; an incorrect answer resets only the active direction.

## Existing learning tracks
- Kana fundamentals remain available as optional review.
- Stage 4 small-っ and long-vowel word practice remains available.
- Stage 5 does not require repeating previously mastered kana or Stage 4 content.

## Progress and publishing
- Keeps the existing localStorage key `kanaAcademy_v1`; no reset is performed.
- Export a backup from Progress details before publishing.
- Extract this ZIP and replace all five files in the GitHub Pages publishing root, then commit.
- The service-worker cache is bumped to v7 so the new app files are fetched.
- Progress is local to the browser/device; keep the exported backup safe.
