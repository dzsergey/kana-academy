# Kana Academy — updated GitHub Pages package

An installable, offline-capable Progressive Web App for hiragana and katakana practice.

## What's new

- **Mixed mode** keeps mastered characters in the pool at a lower selection weight instead of excluding them.
- **Independent mastery by direction:** each character requires 10 consecutive correct answers in Kana → Romaji and, separately, 10 in Romaji → Kana. An incorrect answer resets only the active direction's streak.
- **Three answer directions:** Kana → Romaji, Romaji → Kana, and Random direction (chosen independently for each question).
- **Voiced kana:** optional dakuten and handakuten practice for both hiragana and katakana.
- Progress details show each character's streak/mastery in both directions.

## Progress compatibility

The app deliberately retains the existing localStorage key `kanaAcademy_v1` and the existing top-level `total`, `correct`, `stats`, and `hiraMastered` fields. Existing per-character statistics are retained and extended with `directions.kanaToRomaji` and `directions.romajiToKana` records. The prior app's pre-mastered basic hiragana status is carried forward for Kana → Romaji only; Romaji → Kana mastery is earned separately. No progress is reset during the upgrade.

Before replacing files in a live repository, use **Progress details → Export backup** in the currently installed app as an extra safeguard. Do not clear Safari website data.

## Publish with GitHub Pages

1. Keep a backup of the current repository files.
2. Upload the contents of this ZIP to the repository root, replacing the existing files (do not upload the ZIP itself).
3. In GitHub, open **Settings → Pages** and confirm the existing deployment branch/folder.
4. Wait for the deployment to finish, then open the site in Safari. The updated service worker uses a new cache version and activates the new files.
5. If the Home Screen app still shows the old version, close it fully and reopen it after the site has loaded once in Safari.

## Install on iPhone

Open the published URL in Safari → Share → Add to Home Screen. Enable “Open as Web App” if shown.

## Progress and backup

Progress is stored locally in this browser/device. Use Progress details → Export backup to save a JSON copy; Import backup restores it. There is no automatic cross-device sync. Clearing Safari website data can erase local progress.


## Fix in this update

In Mixed mode, Romaji → Kana questions now draw all answer choices from the same script as the current question. A hiragana question accepts only hiragana; a katakana question accepts only katakana. The service-worker cache version is bumped so browsers fetch the corrected app. Existing progress remains under `kanaAcademy_v1`.


## Stage 3: contracted sounds (yōon)

- Added optional contracted-sound practice for hiragana and katakana, including きゃ/キャ, しゅ/シュ, ちょ/チョ and voiced combinations such as ぎゃ/ギャ, じゃ/ジャ, ぴょ/ピョ.
- Toggle **Include contracted sounds** independently from dakuten/handakuten.
- Mixed mode still chooses one script per question; Romaji → Kana answer choices are restricted to that same script.
- Contracted-sound progress and 10-answer directional mastery are stored under the same `kanaAcademy_v1` key. Existing progress is not reset.
- The service-worker cache is bumped to v4 to ensure the update is fetched.
