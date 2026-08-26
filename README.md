# epassport-web

Product, support and privacy site for **ICAO ePassport Inspector** — an iOS app that performs cryptographic verification of electronic passports on-device.

🌐 **Live:** [epassport-web.vercel.app](https://epassport-web.vercel.app)

## About the app

ICAO ePassport Inspector runs the same cryptographic check used at airport immigration counters, implemented directly against the ICAO 9303 open standard rather than wrapped around a commercial SDK.

| | |
|---|---|
| Protocol | ICAO Doc 9303 Parts 10/11 |
| Trust root | ICAO PKD Master List (CSCA certificates) |
| Secure channel | BAC + PACE (ISO/IEC 14443) |
| Signature | Passive Authentication — RSA · ECDSA · SHA-256 |
| Runtime | iOS 16+ · CoreNFC · Swift |
| Data flow | 100% on-device · zero server calls |

**Flow:** enter or camera-scan the 88-character MRZ (OCR runs on-device) → open a BAC or PACE secure channel with the passport's contactless chip → verify the Document Security Object signature up to a CSCA trust anchor. Verdict in under 15 seconds; on failure no personal information is surfaced.

## Contents of this repo

| File | Purpose |
|---|---|
| `index.html` | Product page — how it works, technology, use cases |
| `getting-started.html` | Bilingual getting-started guide |
| `support.html` | Support page (App Store requirement) |
| `privacy.html` | Privacy policy (App Store requirement) |

Static HTML, deployed on Vercel.

## Privacy

The app collects nothing. No accounts, no analytics, no images or MRZ data leaving the device. See [privacy.html](./privacy.html).

---

ICAO, 9303 and PKD are trademarks of the International Civil Aviation Organization. This application is not endorsed by or affiliated with ICAO.
