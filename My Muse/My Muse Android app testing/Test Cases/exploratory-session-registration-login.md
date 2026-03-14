# Exploratory Testing Session — Android Registration & Login

## Session Details

| Field | Details |
|---|---|
| **Date** | March 13, 2026 |
| **Tester** | Muhammad Nadeem |
| **App** | My Muse v1.0.38 |
| **Platform** | Android |
| **Device** | Android Studio — Android 14 |
| **Network** | Wifi |
| **Session Type** | Exploratory — unscripted, free exploration |
| **Focus Area** | Registration, login, and authentication flows |

---

## Session Charter

> *Explore the My Muse Android app registration and login flows as a brand new user. Focus on: account creation, email handling, password behaviour, error messages, and security of the authentication process. Document all findings, unexpected behaviours, and potential bugs.*

---

## Exploration Log

### Area 1 — Registration Flow

**Actions performed:**
- Navigated to Profile tab → Login → Create Account
- Registered with a real email address I own
- Registered with a fake email address I do not own
- Observed behaviour after each registration attempt
- Checked email inbox for verification emails

**Findings:**

| # | Observation | Type | Severity |
|---|---|---|---|
| 1 | No email verification step after registration — account created and access granted immediately | **Bug** | **P1** |
| 2 | App accepts any email including addresses the tester does not own or have access to | **Bug** (part of #1) | **P1** |
| 3 | Registration requires email and password — no Google or social login options observed | Observation | — |
| 4 | Password field present on Android registration — unlike website which requires no password | Observation — platform difference | — |

---

### Area 2 — Login Flow

**Actions performed:**
- Logged in with correct email and password
- Attempted login with correct email but wrong password
- Attempted login with an email that has never been registered
- Observed error messages for each failed login attempt

**Findings:**

| # | Observation | Type | Severity |
|---|---|---|---|
| 5 | Login with valid credentials works correctly — user redirected to home screen | Expected ✅ | — |
| 6 | Login with wrong password shows clear error message | Expected ✅ | — |
| 7 | Login with unregistered email shows clear error message | Expected ✅ | — |
| 8 | Error messages are user-friendly and descriptive | Expected ✅ | — |

---

### Area 3 — Cross-Platform Authentication Comparison

**Actions performed:**
- Attempted to use Android app credentials on the My Muse website
- Attempted to use the same email on both platforms
- Compared authentication flows between Android and Web

**Findings:**

| # | Observation | Type | Severity |
|---|---|---|---|
| 9 | Android uses email + password — website uses email only — separate auth systems | **Bug** | **P1** |
| 10 | Android credentials do not work on the website | **Bug** (part of #9) | **P1** |
| 11 | Same email blocked on website with silent failure if registered on Android app | **Bug** — see WEB-BUG-002 | **P2** |

---

## Bugs Identified This Session

| Bug ID | Title | Severity | Report |
|---|---|---|---|
| AND-BUG-001 | No email verification on registration — any email accepted, access granted immediately | P1 | [View](bug-reports/AND-BUG-001-no-email-verification.md) |

> **Note:** Cross-platform authentication issues (findings #9–11) are documented under web testing — see **WEB-BUG-003**.

---

## Session Summary

| Metric | Count |
|---|---|
| Areas explored | 3 |
| Total observations | 11 |
| Bugs filed | 1 (P1 × 1) |
| Expected behaviours confirmed | 4 |
| Cross-platform issues identified | 1 |
