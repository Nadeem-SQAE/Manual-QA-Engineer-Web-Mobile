# AND-TC-002 — Verify User Can Successfully Login With Registered Email and Password

## Test Case Details

| Field | Details |
|---|---|
| **TC ID** | AND-TC-002 |
| **Title** | Verify user can successfully login with previously registered email and password |
| **Priority** | P1 |
| **Type** | Functional |
| **Date Executed** | March 10, 2026 |
| **Executed By** | Muhammad Nadeem |
| **Status** | ✅ PASS |
| **Bug Filed** | — |

---

## Environment

| Field | Details |
|---|---|
| **App** | My Muse |
| **App Version** | 1.0.39 |
| **Platform** | Android |
| **Device** | Vivo V2102 |
| **Android Version** | 11 |
| **Network** | Mobile data (4G) |
| **QA Engineer** | Muhammad Nadeem |
| **Date** | March 10, 2026 |

---

## Pre-conditions

- My Muse app is installed on device
- User has a previously registered account with known email and password
- User is NOT currently logged in

---

## Test Data

| Field | Value |
|---|---|
| **Test Email** | 'demo@gmail.com' |
| **Test Password** | '@Demo123' |

---

## Steps

| Step | Action |
|---|---|
| 1 | Open My Muse app on Android device |
| 2 | Tap **Profile** tab in bottom navigation |
| 3 | Tap **"Login"** button |
| 4 | Enter registered email address |
| 5 | Enter correct password |
| 6 | Tap **"Login"** button |
| 7 | Observe login result and current screen |

---

## Expected Result

User is successfully logged in and redirected to the home screen. User's account data including watch history and profile details is accessible.

---

## Actual Result

User was successfully logged in and redirected to the home screen. Watch history and profile details were accessible as expected.
