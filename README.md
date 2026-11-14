# Kana Academy — Stage 4 package

An installable, offline-capable Progressive Web App for hiragana and katakana practice.

## Stage 4: small っ and long vowels

Enable **Include small っ & long-vowel words** to add complete-word reading practice:

- Hiragana small っ: きって (kitte), がっこう (gakkou), きっぷ (kippu), ざっし (zasshi), ちょっと (chotto), まって (matte), いっしょ (issho), けっこん (kekkon), きっさてん (kissaten), もっと (motto).
- Hiragana long vowels: おかあさん (okaasan), おとうさん (otousan), おにいさん (oniisan), おねえさん (oneesan), おおきい (ookii), こうこう (koukou), せんせい (sensei), とうきょう (toukyou), ゆうびん (yuubin).
- Katakana long vowels: コーヒー (koohii), スーパー (suupaa), ケーキ (keeki), タクシー (takushii), ノート (nooto), カード (kaado), チーズ (chiizu), メール (meeru), テーブル (teeburu), スープ (suupu).

The words can be practiced in Kana → Romaji, Romaji → Kana, or Random direction. In Mixed mode, each question belongs to exactly one script. Word questions use word-level distractors from the same script; kana-character questions continue to use kana-character distractors. Every word has independent 10-consecutive-correct mastery in each direction.

## Preserved features

- Basic hiragana and katakana, optional dakuten/handakuten, and optional contracted sounds.
- Mixed mode retains mastered items at a lower frequency.
- Independent mastery in Kana → Romaji and Romaji → Kana.
- Existing progress remains under localStorage key `kanaAcademy_v1`; the prior 416 mastered directions are preserved.
- Stage 4 adds 30 complete words (60 additional possible mastery directions) with fresh progress.
- Service-worker cache bumped to v5.

## Publish

1. In the current app, open **Progress details → Export backup** as a precaution.
2. Extract this ZIP and upload all five files to the root of the GitHub Pages repository, replacing the previous versions.
3. Commit the changes and wait for the Pages deployment to finish.
4. Open the published site in Safari once, then reopen the Home Screen app. Do not clear Safari website data; that can erase local progress.

Progress is stored locally on this device/browser. Use Export backup and Import backup to move it between devices.
