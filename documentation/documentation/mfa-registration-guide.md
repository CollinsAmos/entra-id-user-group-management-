# Task 5: Configuring MFA Registration & Security Questions

## Objective

Strengthen account security by enabling Multi-Factor Authentication (MFA) registration and adding security questions as a password reset verification method.

---

## Part A: Enable MFA Registration Policy

### Step 1: Navigate to MFA Settings

**Path:** `Entra ID → Multifactor authentication`

### Step 2: Configure MFA Registration Policy

| Setting | Value |
|---------|-------|
| Registration required | ✅ All users |
| Methods available | Authenticator app, SMS, Phone call, Email OTP |

### Step 3: End-User Experience

When a user signs in, they see the **"Install Microsoft Authenticator"** page and can:

- Download the app from Google Play or App Store
- Set up a different authentication app
- Continue to the next step once installed

---

## Part B: Configure Security Questions

### Step 1: Navigate to Security Questions

**Path:** `Entra ID → Authentication methods → Password reset → Security questions`

### Step 2: Select Predefined Security Questions

| # | Security Question | Selected |
|---|-------------------|----------|
| 1 | What was the name of the first school you attended? | ✅ Yes |
| 2 | What was the first and last name of your childhood best friend? | ⬜ No |
| 3 | What is your oldest sibling's birthday month and year? | ⬜ No |
| 4 | What is your favorite food? | ⬜ No |
| 5 | What city were you in on New Year's 2000? | ⬜ No |

### Step 3: Configure Number of Questions

| Setting | Value |
|---------|-------|
| Minimum questions required for reset | 2 |
| Number of questions user must register | 3–5 |

### Step 4: Apply to Target Group

- Security questions were applied to `Test-Static-Group`
- Users in this group will be prompted to register their answers on next sign-in

---

## 📸 Screenshot Evidence

- `screenshots/07-security-questions.png` — Predefined security questions selection
- `screenshots/09-mfa-registration.png` — Microsoft Authenticator installation prompt

---

## ✅ Result

- MFA registration is now **required** for all users
- Security questions are available as a password reset method
- Multiple questions provide redundancy and improve user experience

---

## 💡 Best Practices Applied

- **Required MFA for all users** (Microsoft's #1 security recommendation)
- **Selected questions with stable answers** (e.g., "first school")
- **Required 2 questions minimum** for security while maintaining usability
- **Scoped to test group** before wider deployment
