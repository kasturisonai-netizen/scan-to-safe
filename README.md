# Scan to Safe — MVP starter

This is an accessible, mobile-first web/PWA prototype for the Scan to Safe concept.

## Run locally
Open `index.html` in a modern browser. For camera scanning and PWA installation, serve the folder over HTTPS (or localhost).

Example:
```bash
python -m http.server 8000
```
Then open `http://localhost:8000`.

## Included
- English, Hindi, Marathi and Bengali interface translations
- Soft, calming colour palette and responsive layout
- Large controls, visible focus, semantic labels and live status region
- Personal and separate Business inventory modes
- Add/edit/delete products and search
- Expiry status calculation and in-app alerts
- Barcode scanning where the browser supports `BarcodeDetector`
- Voice read-out using the device/browser speech synthesis
- Local JSON export
- PWA manifest and basic offline service worker

## Important MVP limitations
- Data is stored in local browser storage on this device only; there is no account, cloud sync or family sharing yet.
- Barcode scan reads the code only. It does not fetch product details or expiry dates. Expiry dates must be checked on the package and entered by the user.
- Browser barcode detection support varies. Manual entry is always available.
- Notifications are currently requested from the browser and checked when the app is open. Reliable scheduled/background push notifications require a deployed backend and push-notification service.
- The business mode is a separate local inventory view, not yet a multi-user business account or stock-management system.
- This is a prototype, not a production-ready safety or medical product. Users must verify printed dates and follow product-specific storage and disposal guidance.

## Next engineering milestones
1. Supabase authentication, cloud database, row-level security and household/business workspaces.
2. OCR-assisted reading of printed expiry dates, with user confirmation before saving.
3. Product lookup API for barcode metadata (never infer expiry date from barcode).
4. Scheduled notifications and user-configurable reminder windows.
5. Native Android packaging (e.g. Capacitor) and Play Store release process.
6. Accessibility testing with TalkBack, screen magnification, large font settings and older adult usability sessions.
