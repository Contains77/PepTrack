PEPTIDE TRACKER — LOCAL MOBILE WEB APP

Files:
- index.html
- manifest.webmanifest
- sw.js
- icon files

Your starter records are included:
- Retatrutide: 12/07/2026, 1.5 mg, 99.5 kg, no side effects
- Tesamorelin: 13/07/2026, 1 mg, 99.5 kg, side effects left blank

HOW TO RUN LOCALLY ON IPHONE
A web app cannot use offline installation reliably when opened directly as a file.
It needs to be served from localhost or HTTPS.

Simple local-only method:
1. Install a local web-server app on your iPhone, such as a-Shell or iSH.
2. Unzip this folder into the app's accessible folder.
3. Start a local server in that folder:
   python3 -m http.server 8080
4. Open Safari and visit:
   http://localhost:8080
5. In Safari, tap Share > Add to Home Screen.

The app stores data in local browser storage on that phone.
Use Settings > Export backup regularly.
