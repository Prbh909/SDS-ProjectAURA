# SDS Project AURA
## Advanced Unified Ride Assistance

A single-page educational prototype for school bus tracking and smart attendance.

### Included features
- Responsive admin dashboard.
- Interactive Leaflet map with clearly labelled simulated bus routes and positions.
- Demo bus movement button.
- Student directory, search, class filter and add-student workflow.
- QR camera scanner when supported, plus manual student ID lookup.
- Teacher attendance statuses: Present, Absent and Pending review.
- Attendance metrics, class summaries, activity log, CSV export and JSON export.
- Browser-local persistence via localStorage.
- Project settings and an honest status/limitations page.

### Important
This is a front-end prototype. Bus coordinates and student records are fictional. Live GPS, shared multi-user database, secure login, and AI face verification are not connected. QR scanning does not prove who is holding the card. Do not use real student data in a public demo.

### Run locally
Open `index.html` in a modern browser. Internet is needed for Leaflet, map tiles and QR scanner libraries. For camera QR scanning, use HTTPS (GitHub Pages works) or localhost and grant camera permission. If camera scanning does not work, enter demo IDs `SDS1001` through `SDS1008`.

### Publish with GitHub Pages
1. Create a GitHub repository.
2. Upload `index.html` and `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Select **Deploy from a branch**, choose `main` and `/ (root)`, then save.
5. Wait for the Pages URL and open it over HTTPS.

### Teacher demo walkthrough
1. Overview: explain the dashboard and prototype status.
2. Live bus tracking: click **Move demo buses**; explain these are simulated coordinates.
3. Smart attendance: enter `SDS1002`, find the student and mark present or send for review.
4. Mark another student manually using the teacher controls.
5. Students: search/filter the fictional directory.
6. Reports: download the attendance CSV.
7. Project settings: explain AI face verification and real GPS are planned extensions, not falsely claimed as active.

### Path to real deployment
Add authenticated users and a PostgreSQL database with row-level permissions; secure server endpoints for bus GPS; QR tokens with server-side validation and duplicate prevention; and optional face verification only after school approval, appropriate notices/permissions, security evaluation and teacher-review fallback. Mobile browser GPS may pause in the background, so real tracking may require a managed phone and a background-capable app.
