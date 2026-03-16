# AND-TC-001 — Verify App Requires Email Verification Before Granting Access on Registration

## Test Case Details

| Field | Details |
|---|---|
| **TC ID** | AND-TC-001 |
| **Title** | Verify app requires email verification before granting access during registration |
| **Priority** | P1 |
| **Type** | Security / Functional |
| **Date Executed** | March 13, 2026 |
| **Executed By** | Muhammad Nadeem |
| **Status** | ❌ FAIL |
| **Bug Filed** | [AND-BUG-001](bug-reports/AND-BUG-001-no-email-verification.md) |

---

## Environment

| Field | Details |
|---|---|
| **App** | My Muse |
| **App Version** | 1.0.39 |
| **Platform** | Android studio |
| **Device** | Vivo|
| **Android Version** | 11 |
| **Network** | Mobile data (4G) |
| **QA Engineer** | Muhammad Nadeem |
| **Date** | March 13, 2026 |

---

## Pre-conditions

- My Muse app is installed on device
- User is NOT logged in
- Test email has never been registered on My Muse before

---

## Test Data

| Field | Value |
|---|---|
| **Test Email** | `demo@gmail.com` |
| **Test Password** | `@Demo123` |

---

## Steps

| Step | Action |
|---|---|
| 1 | Open My Muse app on Android device |
| 2 | Tap **Profile** tab in bottom navigation |
| 3 | Tap **"Login"** button |
| 4 | Tap **"Create Account"** |
| 5 | Enter email: `demo@gmail.com` |
| 6 | Enter password: `@Demo123` |
| 7 |  Confirm password: `@Demo123` |
| 8 | Click **"Signup"** button |
| 9 | Observe — check if verification message appears on screen |
| 10 | Observe — check if app grants access immediately |
| 11 | Check email inbox — confirm whether verification email was received |

---

## Expected Result

1. App sends a verification email to the provided address
2. App displays message: *"Please verify your email before continuing"*
3. Access is blocked until the user clicks the verification link
4. Account is only activated after email ownership is confirmed

---

## Actual Result

- No verification email sent to the provided address
- No verification message displayed in the app
- User immediately granted access to the app
- Account successfully created  without email verification 
---

## Notes

This is the Android equivalent of **WEB-BUG-001** — the same security vulnerability confirmed across both platforms. Neither the Android app nor the website verifies email ownership before granting access.
