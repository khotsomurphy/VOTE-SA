# VOTE SA — starter prototype

This is a responsive, installable-web-app (PWA) preview intended to run in modern mobile and desktop browsers.

## Included
- Fingerprint-inspired VOTE SA wordmark (visual branding only).
- Overview, public opinion poll, official information, party preview and transparency screens.
- Offline shell caching through a service worker.
- Explicit prototype labels: demo poll response is stored only in the current browser/device.
- IEC and Parliament source links.

## Important limitations
- This is not an official election voting system and is not affiliated with the IEC.
- No legal ballot is cast; no voter registration or identity verification is performed.
- Poll responses are local demo data only. There is no server, cross-device synchronisation, anti-abuse control or live public tally.
- The party screen is a parliamentary-party preview, not the complete IEC register. IEC's party information centre reported 537 registered parties in the research context. Production must import the complete current IEC register with registration level, effective date and source/version metadata.
- No official results API is connected. IEC API access requires credentials. Production integration requires IEC permission/credentials and must preserve source, event, geography, status and timestamps.
- Offline mode can show cached information, but cannot honestly show new live results while disconnected.

## Run locally
Serve this folder over HTTPS or localhost (service workers require a secure context), for example:
`python -m http.server 8000`
Then open `http://localhost:8000`.

## Production architecture recommended
1. Shared cross-platform app: React Native (Expo) or Flutter for iOS and Android.
2. Public polls: separate backend service, poll rules/versioning, rate limiting, abuse prevention, append-only event log, independently reproducible aggregate totals.
3. Official data: read-only IEC integration using authorised credentials; server-side secret storage; signed/verified data ingestion; clear preliminary/final state.
4. Offline: encrypted local cache for public information; queued actions only for public polls, with explicit pending status and server acknowledgement after reconnection. Never represent pending offline entries as live national totals.
5. Directory: scheduled import from the IEC's complete register, with registration level and effective date; publish change history.
6. Security and privacy: independent penetration test, privacy impact assessment, POPIA review, threat model, accessibility testing, backups and disaster recovery.
7. Governance: written IEC engagement/approval for any official election integration; independent oversight and public technical documentation.

## Official references
- IEC: https://www.elections.org.za/
- IEC API information: https://api.elections.org.za/
- IEC API documentation: https://api.elections.org.za/Help
- Parliament party list: https://parliament.gov.za/political-party-list
- IEC party information centre: https://www.elections.org.za/pw/parties-and-candidates/information-centre
