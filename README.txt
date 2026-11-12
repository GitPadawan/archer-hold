ARCHER HOLD — iPhone training timer
==================================

WHAT IT DOES
- Four adjustable settings: sets (1–8), hold duration (5–120 seconds),
  rest duration (5–120 seconds) and weight per dumbbell (1–10 kg).
- Press Start for a 10-second preparation countdown.
- Two high beeps start each hold, one lower beep starts each rest, and
  three rising beeps announce the end of the final hold.
- Rest is between sets, not after the last one.
- Pause, resume and end early; completed holds are recorded.
- Training history is stored on the device, with TXT diary and CSV exports.
- With the PWA hosted on HTTPS, its interface is cached for offline use.

OPEN IT ON A COMPUTER
Open index.html in a regular web browser. The timer and diary should work
without needing to install software. (Browsers may restrict local storage
when opening HTML files directly.)

PUT IT ON AN IPHONE HOME SCREEN
1. Upload the complete contents of this folder (index.html, manifest,
   sw.js and both PNG icons) to a static HTTPS website you control.
   Any static hosting supporting HTTPS works, such as GitHub Pages or
   Netlify Drop. Do not upload just the HTML file if you want offline support.
2. Visit that HTTPS website in SAFARI on your iPhone.
3. Tap Share, then Add to Home Screen, and choose Add.
4. Launch Archer Hold from its new Home Screen icon. Open it once while
   online to let the offline cache install.
5. Tap Test beeps before your first workout and keep the screen awake.
   The app tries to prevent automatic screen locking where supported.

TRAINING LOGS AND PRIVACY
History is stored locally in your browser / installed app. It is not sent
anywhere. Use "History" > "Export diary (.txt)" to save a readable document
or "Export CSV" for Apple Numbers / Excel. Save the exported file to Files,
iCloud Drive, or share it with Notes. Removing the installed app or clearing
website data can delete the local history. Safari and a standalone Home
Screen app may maintain separate storage; do your sessions in one location.

IMPORTANT LIMITATIONS
- Web timers and sounds cannot be guaranteed when an iPhone screen is locked
  or the app is in the background. Archer Hold automatically PAUSES when it
  detects going into the background. Keep Archer Hold foregrounded.
- On iPhone, sound can be affected by silent mode, audio volume, and device
  browser policies. Test the beeps first and adjust device audio settings.
- This is a training timer, not a calibrated bow-force simulator: an
  outstretched dumbbell is mechanically different from an archery draw.
- Start with a comfortable load and avoid shoulder pain or locked joints.

All functionality runs locally in JavaScript. No accounts, ads, analytics,
external APIs or online database are included.

EXACT GITHUB PAGES INSTALLATION (MAC / PC)
=========================================
1. Download the ZIP and double-click it to unzip. Open the 'archer-hold' folder.
2. Sign in at https://github.com (a free account is fine).
3. Click + (upper-right) > New repository. Name: archer-hold.
   Choose Public, then click Create repository.
4. Click 'uploading an existing file' in the empty repo, or
   Add file > Upload files if that button is displayed.
5. Select the files INSIDE the unzipped archer-hold folder and drag them to
   the upload page: index.html, sw.js, manifest.webmanifest, icon-192.png,
   icon-512.png (README.txt optional). Do not upload the ZIP or the outer
   folder. index.html must appear at the repository's top level.
6. Select 'Commit directly to the main branch' if shown, then Commit changes.
7. Click Settings in the repository > Pages in the left sidebar.
8. Under Build and deployment, set Source: Deploy from a branch.
   Select branch main and folder /(root), then click Save.
9. Once published, return to Settings > Pages and choose Visit site.
   Your website should be https://YOUR-USERNAME.github.io/archer-hold/
   (replace YOUR-USERNAME with the GitHub account username).

ON IPHONE
=========
10. Open the published URL in Safari (not the GitHub code page).
11. Open Share > Add to Home Screen, switch on Open as Web App if shown,
    and tap Add.
12. Open Archer Hold from your Home Screen once while online, then
    press Test beeps. Keep the screen active during workouts.
13. To review or back up workouts, tap History > Export diary (.txt)
    or Export CSV. History is stored on your iPhone, not GitHub.

IF IT DOESN'T OPEN
=================
- If it shows 404, check GitHub Settings > Pages for publication status.
- Check that index.html is at the TOP LEVEL, not in a folder inside the repo.
- Check Pages is set to main / (root), not None.
- This is a public website; only the app code is uploaded, not your diary.

AUDIO PATCH v1.1 (2026-11-12)
=============================
CHANGES
- Requests an iOS media playback audio session, which can allow Web Audio
  beeps even when the iPhone is in Silent Mode (supported iOS versions).
- Primes Web Audio on a direct tap for better iPhone compatibility.
- Fixes the completion beep not being played at the end of the final set.
- Changes the service worker cache identifier from v1 to v2, so existing
  installed Archer Hold apps can retrieve the updated app.

UPDATE AN EXISTING GITHUB PAGES INSTALLATION
1. Open your GitHub repository (GitPadawan/archer-hold) on your computer.
2. Add file > Upload files. Upload ONLY these two replacement files from
   this audio-fix folder: index.html and sw.js. Commit the changes to main.
3. In iPhone Safari, open https://gitpadawan.github.io/archer-hold/ while
   connected to the internet; close and reopen Archer Hold from its Home
   Screen icon. The updated setup screen says 'Archer Hold v1.1' at bottom.
4. Press Test beeps and keep the phone screen on. If it remains silent,
   temporarily turn off Silent Mode and increase media volume.

IMPORTANT: These are only client-side files. No settings or history keys were
changed, so your existing training history should remain. Do not delete the
Home Screen app or clear its website data to update, as that can erase logs.

Some iOS versions still have Web Audio bugs that cannot be fully fixed by
website code.


Archer Hold v1.2 — triple completion beep
----------------------------------------
When the final hold finishes, Archer Hold plays THREE clearly spaced beeps.
The regular double-beep start and single rest cue are unchanged.
On the setup screen, tap “Test finish” to preview the three beeps.

Updating an existing GitHub Pages installation:
1. In your repository, replace index.html and sw.js with the two v1.2 files.
2. Commit the changes to the main branch.
3. After GitHub Pages finishes publishing, open your Archer Hold website in Safari.
4. Close and reopen the Home Screen app (sometimes twice after a service-worker update).
5. Check that the setup footer reads Archer Hold v1.2.
Your saved training history is retained; do not delete the existing Home Screen app.
