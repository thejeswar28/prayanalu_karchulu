Prayanalu🥳 - Karchulu😔 Android project (version 1.4)

Changes in this update:
- Edit existing expenses (description, amount, payer, category, date, split members).
- Delete expenses from the expense list.
- Download CSV report.
- Download Excel-compatible .xls report (SpreadsheetML; opens in Microsoft Excel).
- Android downloads are saved through the native Android bridge to Downloads/PrayanaluKarchulu.

Build a new APK with GitHub Actions:
1. Replace the files in your existing GitHub repository with the contents of this ZIP. Keep the .github/workflows/build-apk.yml path at repository root.
2. Commit/push the changes to the main branch, or open Actions -> Build Android APK -> Run workflow.
3. Wait for the workflow to finish successfully.
4. Open the workflow run, download artifact Prayanalu-Karchulu-APK, and extract app-debug.apk.
5. Install the new APK. It uses the same application ID, so it should update the existing app and preserve local data; still export a backup before updating.

This ZIP is source code, not a compiled APK. The workflow builds a debug APK for personal use.

Version 1.2 review fixes: expense search, local date handling, exact paise split rounding, safer CSV cell escaping, and protection against deleting members who have paid historical expenses.

Version 1.3: Member names are displayed in the selected language script using offline phonetic transliteration. The original saved name is preserved; switching language never overwrites stored names. Transliteration is approximate for proper names, so verify spellings.


Version 1.4 features:
- Member expense history: select a member to see expenses they paid, their share in expenses, and their advance deposits.
- Advance payments: record a member's trip advance. It is treated as a credit in the member balance and settlement (not as trip spending).
- Custom expense splits: Equal, Percentage (must total exactly 100.00%), or Individual amounts (must total exactly the expense amount to the paise).
- Existing v1.3 data is migrated in memory with equal split defaults and empty advance lists; existing data format remains compatible.

Important: Before installing an update, export a backup from the app. This is a source project, not a compiled APK.


Version 1.5 update: Smart Split is integrated in the existing expense form as four in-place choices: Equal, Percentage, Exact Amount, and Shares (ratio). Existing expense records remain compatible; old records default to Equal split.
