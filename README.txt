KATANA OS PWA PACKAGE

FILES
- index.html                 Current Katana OS build
- manifest.json              Android/PWA install metadata
- sw.js                      Offline shell + notification service worker
- okatan-icon-192.png        PWA icon
- okatan-icon-512.png        PWA icon
- okatan-icon-maskable-512.png Android adaptive/maskable icon

IMPORTANT
A service worker cannot run from file://.
To install Katana OS as a PWA, serve this folder over HTTPS (or localhost).

QUICK TEST ON A COMPUTER
1. Open a terminal in this folder.
2. Run: python -m http.server 8080
3. Open http://localhost:8080
4. Chrome/Edge should offer Install App.

PHONE
Host the folder on an HTTPS static host (GitHub Pages, Cloudflare Pages, Netlify,
your own HTTPS server, etc.), open the HTTPS URL in Chrome on Android, then use
Install app / Add to Home screen.

OFFLINE
The Katana shell itself is cached after the first successful load. Features that
depend on remote APIs, external websites, maps, AI providers, or live data still
need internet unless their own code supports offline operation.
