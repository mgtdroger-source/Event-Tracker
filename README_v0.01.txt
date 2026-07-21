TD6 Entrant Tracker TEST v0.01

PURPOSE
First real-phone road test of the fenced TD6 tracking pipeline.
This package is separate from production STC Recorder v2.59.

PRECONFIGURED TEST IDENTITY
Rally number: 37
Driver: Roger Lewis
Event ID: RID-20260708-LX1ZH7
Rally title: Deep South 2026
Route identity: Route 1
Report interval: 30 seconds

PACKAGE FILES
- index.html
- manifest.webmanifest
- service-worker.js
- tracker-config.json
- icon-192.png
- icon-512.png

TEST FLOW
1. Upload the complete package to a separate GitHub Pages test repository/folder.
2. Open the HTTPS link on the Android phone.
3. Install/add the PWA if desired.
4. While stationary, open the app and select Start Tracking.
5. Allow precise location access.
6. Confirm GPS ready and a successful Last sent time.
7. Leave the phone powered, screen on and brightness low for this first trial.
8. Do not operate the phone while driving.
9. At the destination, select Stop Tracking.
10. Later open TD6 Event Tracking TEST v0.15, load the usual test route, and use Find Entrant 37.

BEHAVIOUR
- Sends the latest GPS fix every 30 seconds.
- First usable GPS fix is sent immediately after Start Tracking.
- Reports are queued in localStorage if a send fails or the phone is offline.
- Queued reports retry when connectivity returns.
- GPS capture time is retained for delayed reports.
- Requests a screen wake lock where supported.
- This first build deliberately avoids STC, timing, daily validity and route logic.

IMPORTANT FIRST-TEST LIMITATION
Mobile browsers can restrict background activity. For this first road test, keep the PWA visible with the screen on and brightness reduced.
