## Lab 1: Setting Up and Securing Your GitHub Account
**Real-World Scenario:** It's a new hire's first day, and IT has asked them to complete account setup — enabling two-factor authentication and generating a token for any tools that will need to authenticate on their behalf — before they're granted access to any team repositories.
**Why we are doing this:** Proper account setup, done through the account Settings UI, ensures secure access from day one and gives an administrator the credentials needed to configure tools and integrations without ever sharing a password.

### Step-by-Step Instructions:
1. **Sign In and Confirm Your Email:**
   * On `github.com`, sign in with your account.
   * Click your profile photo, select `Settings`, then click `Emails` in the left sidebar.
   * Confirm your primary email address shows as verified. If it does not, click `Resend verification email` and complete verification.
2. **Review Your Public Profile Name:**
   * Click `Public profile` in the left sidebar and confirm your display name is filled in.
   * *Explanation:* Unlike local Git, which requires separately configuring a name and email with `git config`, any change you make through the web editor is automatically attributed to your verified GitHub account — one less thing an admin has to keep in sync.
3. **Enable Two-Factor Authentication:**
   * Click `Password and authentication` in the left sidebar.
   * Click `Enable two-factor authentication`, choose an authenticator app, and complete setup by scanning the QR code and entering the generated code.
4. **Save Your Recovery Codes:**
   * When prompted, download or copy your recovery codes and store them somewhere safe.
   * *Explanation:* Recovery codes are the only way back into your account if you lose your authenticator device — every admin should know exactly where theirs are.
5. **Generate a Personal Access Token:**
   * Click `Developer settings` at the bottom of the left sidebar, then `Personal access tokens`, then `Fine-grained tokens`.
   * Click `Generate new token`.
6. **Configure the Token's Scope:**
   * Give it a descriptive name, such as "Practice Token".
   * Set an expiration date (30 days is fine for this exercise).
   * Under `Repository access`, select `Only select repositories` and choose one repository you own.
   * Under `Permissions`, expand `Repository permissions` and set `Contents` to `Read and write`.
   * *Explanation:* Fine-grained tokens let you scope exactly what a tool or script can touch — a token for one repository with read/write on contents can't be used to delete an unrelated repository or change account settings.
7. **Generate and Store the Token:** Click `Generate token`, then copy the token value immediately and store it somewhere safe — GitHub will not show it to you again.
8. **Verify the Token Is Listed:** Return to `Personal access tokens > Fine-grained tokens` and confirm your new token appears with the correct name, expiration, and scope.
9. **Register an SSH Key:**
   * Click `SSH and GPG keys` in the left sidebar, then `New SSH key`.
   * Give it a descriptive title, such as "Build Server" or "Practice Key".
   * Paste a sample public key value provided by your instructor into the `Key` field, and click `Add SSH key`.
   * *Explanation:* In practice, the key pair itself is generated on whichever machine or server needs to authenticate; as an administrator, your role is most often registering a public key someone else generated — exactly this step.
10. **Verify the Key Is Registered:** Confirm the key now appears in your `SSH and GPG keys` list with the correct title and fingerprint.
11. **Verify:** Confirm two-factor authentication shows as `Enabled`, your fine-grained token appears in the token list with the correct scope, and your SSH key is listed — all without ever opening a terminal.

---
