```markdown
# CC REMINDER

Simple Android local app to save customers (name, phone, address, remark) and set a reminder date. Notifications fire at 11:00 AM on the chosen date.

How to use this repo to get APK (quick steps):

1. Create a new repository on GitHub (name: cc-reminder) or use an existing one.
2. Clone it locally:
   - git clone https://github.com/YOUR_USERNAME/cc-reminder.git
   - cd cc-reminder
3. Copy the files/folders from this repo content into the cloned folder.
   - Make sure the Android project has gradlew, gradle/wrapper/* files. If not, open Android Studio and create a new project, then replace the `app/` module with the files above.
4. Commit & push:
   - git add .
   - git commit -m "Initial commit: CC REMINDER"
   - git push origin main
5. Open GitHub -> repository -> Actions tab. The "Build APK" workflow will run automatically on push.
6. Open latest workflow run -> find "Artifacts" section -> download `app-debug-apk`.
7. Extract the downloaded artifact (if zipped) to get `app-debug.apk`.
8. Transfer APK to your Android device and install (allow unknown sources if needed).

Notes:
- The build produces a debug APK. For Play Store release you must create a signing keystore and configure release signing.
- If you don't have the gradle wrapper files, either add them or generate via Android Studio: File -> New Project to create wrapper; copy wrapper files into this repo.
- If alarms/notifications not firing after reboot, consider adding a BootReceiver to reschedule stored reminders.
```