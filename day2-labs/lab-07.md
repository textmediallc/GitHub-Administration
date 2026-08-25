## Lab 7: Configuring Organization Security Settings and the Audit Log
**Real-World Scenario:** Your organization is about to bring on its first outside contractors, and leadership wants every member — employee or contractor — held to the same baseline security requirements.
**Why we are doing this:** Organization-wide security settings and the audit log are how an administrator enforces and later verifies a consistent security baseline, rather than trusting each individual member to configure their own account correctly.

### Step-by-Step Instructions:
1. **Open Your Organization:** Navigate to the organization from Lab 5, then click `Settings`.
2. **Open Authentication Security:** Click `Authentication security` in the left sidebar.
3. **Review Two-Factor Authentication Enforcement:**
   * Locate the option to require two-factor authentication for all members.
   * Read the warning about members who don't yet have 2FA enabled, without enabling the requirement yet in this shared practice organization.
   * *Explanation:* Enforcing this immediately would remove any member without 2FA already enabled — in a real rollout, you'd first confirm every current member has 2FA on, then enable enforcement.
4. **Review SAML Single Sign-On:** Still under `Authentication security`, review the SAML SSO configuration section and note the fields it requires (identity provider URL, certificate) without completing setup, since this requires a real identity provider.
5. **Review Member Privileges Again:** Click `Member privileges` and confirm the base permission level set in Lab 5 is still `Read`.
6. **Review Third-Party Application Access:**
   * Click `Third-party access` in the left sidebar.
   * Review the setting for requiring administrator approval before any OAuth application can access organization data.
7. **Open the Audit Log:** Click `Audit log` in the left sidebar.
8. **Review Recent Events:** Scan the list of recent events, which should include the team creation and repository actions from Labs 5 and 6.
9. **Filter the Audit Log:**
   * In the search bar, enter `action:team.add_member` and press Enter.
   * Confirm the entry from adding yourself to the `backend` team in Lab 6 appears.
10. **Filter by Actor:** Clear the filter and enter `actor:your-username` to see every action attributed to your own account.
11. **Filter by Date:** Add a date qualifier, such as `created:>2026-01-01`, and confirm results narrow accordingly.
12. **Verify:** Confirm you can locate, in the audit log, the exact event recording when `backend` was granted access to `org-service-lab` in Lab 6, including the timestamp and actor.

---
