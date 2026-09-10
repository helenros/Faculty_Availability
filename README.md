# Faculty Availability System — Final Netlify Version

## What this version does
- Faculty search and current availability
- BKC/BCC campus filter
- Live current date/time
- Available Now dashboard
- Weekly timetable
- Administrator password
- Excel timetable upload from browser
- Central persistent timetable using Netlify Blobs
- Server-side Excel parsing using SheetJS
- Netlify Functions API

## Deploy
1. Create a GitHub repository and upload all files in this folder.
2. In Netlify: Add new project → Import an existing project → choose the repository.
3. Netlify detects `netlify.toml`.
4. In Netlify Project Configuration → Environment variables, create:
   `ADMIN_PASSWORD` = a strong private password.
5. Redeploy.
6. Open your Netlify URL.
7. Open Administrator → enter the password → upload the next timetable Excel.

## Security
- Never put ADMIN_PASSWORD in source code.
- Change it if it is ever shared.
- Only administrators who know the password can publish a new timetable.

## Excel format
The parser expects sheets named BKC and/or BCC, with faculty blocks containing:
`Name of the Faculty: ...`
followed by a `Days` row and four timetable periods.
