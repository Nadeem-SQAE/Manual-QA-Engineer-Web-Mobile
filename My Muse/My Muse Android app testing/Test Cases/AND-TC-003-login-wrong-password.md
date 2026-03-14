# AND-TC-003 — Verify App Displays Error When Login Attempted With Wrong Password

## Test Case Details

| Field | Details |
|---|---|
| **TC ID** | AND-TC-003 |
| **Title** | Verify app displays a clear error message when user attempts login with incorrect password |
| **Priority** | P2 |
| **Type** | Functional / Error Handling |
| **Date Executed** | March 16, 2026 |
| **Executed By** | Muhammad Nadeem |
| **Status** | ✅ PASS |
| **Bug Filed** | — |

---

## Environment

| Field | Details |
|---|---|
| **App** | My Muse |
| **App Version** | 1.0.38 |
| **Platform** | Android studio |
| **Android Version** | 14 |
| **Network** | Wifi |
| **QA Engineer** | Muhammad Nadeem |
| **Date** | March 16, 2026 |

---

## Pre-conditions

- My Muse app is installed on device
- User has a previously registered account with known email
- User is NOT currently logged in

---

## Test Data

| Field | Value |
|---|---|
| **Test Email** | Previously registered QA test account email |
| **Test Password** | `WrongPassword123` — intentionally incorrect |

---

## Steps

| Step | Action |
|---|---|
| 1 | Open My Muse app on Android device |
| 2 | Tap **Profile** tab in bottom navigation |
| 3 | Tap **"Login"** button |
| 4 | Enter registered email address |
| 5 | Enter incorrect password: `WrongPassword123` |
| 6 | Tap **"Login"** button |
| 7 | Observe error message displayed on screen |

---

## Expected Result

App displays a clear error message such as: *"Incorrect password. Please try again."* User remains on the login screen and access is not granted.

---

## Actual Result

App displayed an error message informing the user that the password was incorrect. User remained on the login screen. Access was not granted.
