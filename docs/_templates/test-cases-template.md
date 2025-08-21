# Test Cases · <Project>


## TC-001 Login with valid credentials
**Preconditions**
- User exists, password known


**Steps & Expected**
| Step | Expected |
| --- | --- |
| Open login page | Page loads, fields visible |
| Enter valid email and password | Inputs accept values |
| Submit | 200 OK, redirect to dashboard, session cookie present |


## TC-002 Login with locked user
**Preconditions**
- Account is locked


**Steps & Expected**
| Step | Expected |
| --- | --- |
| Open login page | Page loads |
| Enter locked email + valid password | Accepted |
| Submit | Error message displayed, no session |


## TC-003 Contact form over limit
**Steps & Expected**
| Step | Expected |
| --- | --- |
| Open contact form | Visible |
| Paste 5,000+ chars message | Client validation blocks |
| Submit | Request prevented, clear validation message |