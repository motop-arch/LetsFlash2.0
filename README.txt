LETSFLASH — GITHUB-READY ANDROID SOURCE

This is the complete editable source project for LetsFlash. It is not an APK;
GitHub Actions compiles the APK.

INCLUDED
- index.html: app interface and application logic
- native-bridge.js: Android native backup/share bridge
- package.json and capacitor.config.json
- letsflash-logo.png and assets/icon-only.png
- .github/workflows/build.yml: GitHub Actions workflow
- sample-data.csv and sample-data.json: import templates

FEATURES RETAINED
- Offline-first IndexedDB storage
- Separate decks; CSV, TXT and JSON imports
- Add, edit, delete and rename decks/cards
- Chinese front, Pinyin, meaning, optional translation
- Explanation, example Hanzi, example Pinyin, example translation, grammar and notes
- Optional image/audio URLs or data URIs and phone attachment
- Reveal-answer study flow, previous/next, shuffle and restart
- Optional Chinese typing practice
- Again / Hard / Good / Easy ratings and configurable review intervals
- Dark/light themes and custom background colour
- Full backup export/restore and individual deck JSON export
- Android launcher icon and native share/export support

CSV HEADERS
front,pinyin,meaning,translation,explanation,example,example_pinyin,example_translation,grammar,category,image,audio,notes

Common alternate headers are recognised, including Chinese (Hanzi), Example (Hanzi),
Example (Pinyin), Example (Meaning), word, english, example_sentence, sentence_pinyin,
grammar_pattern, image_url and audio_url. Quote CSV cells containing commas, quotes or
line breaks. Leave image/audio blank until you add media.

NOTE ABOUT THE EARLIER HSK1 CSV FILES
Some rows in the supplied HSK1 export place Traditional Hanzi in the Pinyin column and
Pinyin in the Meaning column. The importer conservatively repairs obvious Hanzi/Pinyin
swaps, but it cannot infer missing English word meanings. Review or regenerate those
rows rather than treating their meaning column as verified.

UPLOAD AND BUILD
1. Extract this ZIP.
2. Create a GitHub repository.
3. Upload the CONTENTS of this folder to the repository root (not the ZIP itself).
4. Confirm .github/workflows/build.yml is present.
5. Commit to the main branch.
6. Open the repository Actions tab and select Build LetsFlash APK.
7. Open the latest successful run and download letsflash-debug-apk.
8. Extract that artifact ZIP and install app-debug.apk on your Android phone.

BUILD DETAILS
- Builds a debug APK on GitHub-hosted Ubuntu.
- Android application ID: com.surjo.letsflash.
- No local Android Studio installation is needed for this workflow.
- Study data is stored locally on each device. Export a backup before uninstalling or
  clearing app data.
- Play Store distribution requires a separately signed release build.

The app maps example_pinyin through CSV/JSON import, card editing and the answer display.
Image and audio functionality remains available and optional.
