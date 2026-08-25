# Normalsider for Microsoft Word

Minimalistisk Word-tilføjelse, der viser antal normalsider.

Beregning:
antal tegn inkl. mellemrum / 2400

Standardvisningen viser kun normalsidetallet. Under indstillinger kan
"Medtag tekstbokse" slås til. Indstillingen gemmes lokalt i brugerens browser/webview.

Fodnoter, slutnoter, sidehoveder og sidefødder er ikke en del af dokumentets
body og medregnes derfor ikke.

## Task pane-bredde

Tilføjelsen forsøger at sætte task pane-bredden via Office TaskPane API, hvor API'et
er tilgængeligt. Word på Windows/Mac har lavere minimumsbredde end Word på web.

## Lokal test

Installer Node.js:
npm install --global http-server office-addin-dev-certs
npx office-addin-dev-certs install

Kopiér localhost.crt og localhost.key til denne mappe og start:
http-server -S -C localhost.crt -K localhost.key --cors . -p 3000

Sideload manifest.xml i Word.
