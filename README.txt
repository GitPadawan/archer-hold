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
