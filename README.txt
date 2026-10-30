Prayanalu🥳 - Karchulu😔 Android wrapper project

This is source code for an Android WebView app that bundles the offline HTML prototype.
It is NOT a compiled APK.

Build APK with GitHub Actions:
1. Create a new GitHub repository using Chrome on your phone.
2. Upload the contents of this project (including hidden .github/workflows/build-apk.yml).
3. Push to the main branch, or open Actions -> Build Android APK -> Run workflow.
4. Wait for the workflow to finish successfully.
5. Open the completed workflow run, download the artifact named Prayanalu-Karchulu-APK, and extract app-debug.apk.
6. Open the APK on your Android phone and allow installation from that source if Android asks.

Notes:
- This creates a debug APK, suitable for personal testing, not Play Store publishing.
- Expenses are stored locally in app WebView storage. Use the app's backup/export feature regularly.
- The app has no account sync. Clearing app data or uninstalling may remove locally stored records.


Workflow fix (Oct 2026): uses android-actions/setup-android@v4 and explicitly installs platform-tools. The old v3 action attempted to install the retired SDK package named tools, causing the error “Failed to find package tools”.
