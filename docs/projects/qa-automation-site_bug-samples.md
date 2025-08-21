# QA Automation Site · Bug Samples


## Bug 1 · Locked user gets success response
**Steps**
1. Open /login
2. Enter locked_user@example.com with valid password
3. Submit


**Actual**
- UI displays “Welcome” and navigates to dashboard


**Expected**
- Error message for locked account, dashboard not accessible, no session cookie


**Environment**
- Browser: Chromium 128, Firefox 129
- OS: Windows 10, macOS 14
- Build: <hash>


**Severity**
- Major


**Notes**
- Playwright trace: artifacts/trace.zip


## Bug 2 · Contact form accepts 10,000+ chars causing 413
**Steps**
1. Open /contact
2. Fill valid name and email
3. Paste 12,000 char message
4. Submit


**Actual**
- Frontend sends request, backend returns 413, UI shows generic error


**Expected**
- Client‑side validation blocks over 5,000 chars and shows clear message


**Environment**
- Browser: Chromium 128 · OS: Windows 10


**Severity**
- Average


## Bug 3 · /auth/login returns 200 with error payload
**Steps**
1. POST /auth/login with invalid credentials


**Actual**
- 200 with `{ "error": "invalid_credentials" }`


**Expected**
- 401 with error payload, cache headers disabled


**Environment**
- Tool: Playwright request


**Severity**
- Major