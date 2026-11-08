# Kiki's Glam Studio – Android app

This repository builds the Android app for Google Play. The game itself is copied in
automatically from https://github.com/VSZANZ/VSZANZ.github.io each time you build.

## One-time setup
1. Repository **Settings → Secrets and variables → Actions → New repository secret**:
   - `KEYSTORE_BASE64` – the whole contents of `KEYSTORE_BASE64.txt`
   - `KEYSTORE_PASSWORD` – the password in `KEY-INFO-KEEP-PRIVATE.txt`
2. Never upload the `.jks` key file or the key info file to GitHub.

## Build the app
1. **Actions → Build Android app → Run workflow**.
2. Version code: `1` the first time, then `2`, `3`, … for every new upload. Version name: e.g. `1.0.0`.
3. When the run shows a green tick (about 5 minutes), open it and download the file under **Artifacts**.
4. Unzip it: upload the `.aab` to Play Console. The `.apk` is for installing on your own phone to test.

## Updating the game
Change the game in the `VSZANZ.github.io` repository, then run the workflow again with a higher version code.
