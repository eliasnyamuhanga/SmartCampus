# SmartCampus — Campus Issue Reporting Web App

A responsive HTML/CSS/JavaScript prototype that lets students report campus infrastructure and environmental problems, attach photos/videos, view report history, filter reports, and share a report summary through WhatsApp.

## Run it
1. Extract `SmartCampus.zip`.
2. Open the `SmartCampus` folder.
3. Double-click `index.html` (or use VS Code Live Server).
4. Test by submitting a report with a photo or video.

No build tools or installation are required.

## Connect your campus WhatsApp
Open `app.js` and find:

```js
const WHATSAPP_NUMBER = "255700000000";
```

Replace it with the official campus office number in international format, digits only. For example, Tanzania numbers start with `255`. Do not include `+`, spaces or hyphens.

When the student shares a report, WhatsApp opens with the report details pre-filled. On supported mobile browsers, the app may offer native file sharing for attached evidence. Otherwise the student must attach the image/video manually in WhatsApp. A `wa.me` text link cannot silently upload media.

## Important prototype limitations
- Reports are saved in the browser's `localStorage` on the device used to submit them.
- This is a front-end prototype, not a live multi-user reporting system. Reports are not automatically sent to university staff or visible on another student's device.
- To launch for real, connect a secure backend (for example FastAPI + PostgreSQL/SQLite), authentication, file storage, administrator dashboard, notifications and role-based access.
- Do not publish private student information or sensitive evidence publicly. Establish a campus reporting and privacy policy before deployment.
- For emergencies, students should contact campus security or emergency services directly.

## Files
- `index.html` — page structure
- `styles.css` — responsive interface and visual design
- `app.js` — report form, local storage, media preview, filters and WhatsApp sharing
