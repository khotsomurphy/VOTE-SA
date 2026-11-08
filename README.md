# VOTE SA — installable web-app package

#Read and write permission to chatGPT
This package is a mobile-friendly Progressive Web App (PWA) starter. It includes the VOTE SA prototype, fingerprint-style app icons, a web app manifest, and offline caching.

## Install it on a phone

**Important:** A ZIP file opened directly from Downloads is only a source package. For the full app-style installation, the folder must first be published to a secure HTTPS website. The package is ready for that hosting step, but it has not been published to a website by this project.

### Android (Chrome)
1. Publish the contents of this folder to an HTTPS website.
2. Open that website in Chrome on your Android phone.
3. Tap the three-dot menu, then choose **Install app** or **Add to Home screen**.
4. Confirm. The VOTE SA icon will appear on your home screen.

### iPhone (Safari)
1. Publish the contents of this folder to an HTTPS website.
2. Open the website in Safari.
3. Tap **Share** → **Add to Home Screen** → **Add**.

## What is included
- `index.html`: responsive VOTE SA interface.
- `manifest.webmanifest`: install name, display mode, colours and icons.
- `sw.js`: caches the app shell and icons for offline reopening after the first successful visit.
- `icons/`: 192px, 512px and Apple touch icons.

## Important product and safety limits
- This is a prototype, not an official IEC product and not a legally binding voting service.
- Public poll responses are saved only in the current browser/device. They are not sent to a shared server and there is no live national tally.
- The party list is a limited preview, not the full current IEC register.
- The official results panel is not connected to an IEC feed.
- The fingerprint is artwork only. The app does not collect fingerprint/biometric data.
- Offline mode can show cached content; it cannot receive live updates while disconnected.

## Hosting checklist
- Upload the contents of this folder (not the ZIP itself) to an HTTPS static host.
- Keep `index.html`, `manifest.webmanifest`, `sw.js` and the `icons/` directory at the same relative paths.
- Confirm the host serves `manifest.webmanifest` with a JSON-compatible content type and allows service workers.
- Test installation and offline reopening on a real device.

## Next production steps
A shared poll backend, moderation and abuse controls, a complete IEC party-register import, authorised read-only IEC data integration, privacy/security review, accessibility testing, and app-store packaging are still required. Do not add legal ballot casting or biometric voter identification without the appropriate IEC authority and legal approvals.
