## Lab 12: Managing Account Security — Two-Factor Authentication, Sessions, and the Security Log
**Real-World Scenario:** As part of a routine security review, your organization's IT lead has asked every admin to confirm their own account is properly secured and to know where to look if an account is ever suspected of being compromised.
**Why we are doing this:** GitHub administrators are frequently the first people asked to investigate a suspicious login or access request. Knowing where these controls live in the UI — before an incident happens — is essential.

### Step-by-Step Instructions:
1. **Open Your Account Settings:** On `github.com`, click your profile photo in the top-right corner, then select `Settings`.
2. **Review Two-Factor Authentication Status:**
   * Click `Password and authentication` in the left sidebar.
   * Confirm whether two-factor authentication shows as `Enabled`. If it is not, click `Enable two-factor authentication` and complete the setup using an authenticator app.
3. **View Your Recovery Codes:**
   * Under the two-factor authentication section, click `View your recovery codes`.
   * Re-enter your password if prompted, and confirm the codes are visible.
   * *Explanation:* Recovery codes are the only way back into your account if you lose access to your authenticator app — administrators should know exactly where to find them.
4. **Review Authorized OAuth Applications:**
   * Click `Applications` in the left sidebar, then the `Authorized OAuth Apps` tab.
   * Review the list of third-party applications with access to your account.
5. **Revoke an Unused Application (If Any):** If you see an application you no longer use or don't recognize, click it and select `Revoke access`.
   * *Explanation:* Every authorized application is a potential access path into your account — periodically reviewing this list is a basic security hygiene task.
6. **Review Active Sessions:**
   * Click `Sessions` in the left sidebar.
   * Review the list of devices and locations currently signed in to your account.
7. **Sign Out of an Unrecognized Session (If Any):** If any session looks unfamiliar, click `Sign out` next to it.
8. **Open the Security Log:**
   * Click `Security log` in the left sidebar.
   * Review the list of recent security-relevant events on your account (sign-ins, permission changes, SSH key additions, etc.).
9. **Filter the Security Log:**
   * In the search bar at the top of the log, type `action:oauth_authorization` and press Enter to filter to just OAuth-related events.
   * Clear the filter, then try `action:two_factor_authentication` to see 2FA-related events.
10. **Verify:** Confirm you can explain, in one sentence each, where you would look to (a) confirm 2FA is enabled on an account, (b) see every device currently signed in, and (c) investigate a suspicious recent change.

---
