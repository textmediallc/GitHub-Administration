## Lab 5: Enabling Secret Scanning and Investigating an Alert
**Real-World Scenario:** A developer on your team accidentally committed a placeholder API key to a configuration file, and you need to find and confirm it before it becomes a real problem.
**Why we are doing this:** Enabling secret scanning and knowing how to read a generated alert is the first step in catching credential leaks before they're exploited.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Enable Secret Scanning:** Click `Settings`, then `Code security`, and click `Enable` next to `Secret scanning`.
3. **Create a Test File with a Recognizable Pattern:**
   * Click `Add file`, then `Create new file`, and name it `config/sample.env`.
   * Add the line `AWS_ACCESS_KEY_ID=AKIAIOSFODNN7EXAMPLE` (a widely used, publicly documented example AWS key format, safe for training purposes).
4. **Commit the File:** Commit directly to `main`.
5. **Wait for the Scan:** Give GitHub a few moments to scan the new commit, then navigate to `Security`, then `Secret scanning alerts`.
6. **Open the Alert:** Click into the alert generated for your test credential.
7. **Review the Alert Detail:** Note which file and line the secret was found in, and which partner pattern (AWS) it matched.
8. **Check the Validity Status:** Look for an indicator of whether GitHub was able to validate the key as currently active (this specific example key is a widely published placeholder, so it should show as not active).
9. **Remove the Test Secret:**
   * Edit `config/sample.env`, delete the line containing the fake key, and commit the change.
10. **Confirm the Alert State Updates:** Return to `Security > Secret scanning alerts` and confirm the alert reflects that the secret is no longer present in the current file, though it remains in history.
11. **Verify:** Confirm you can explain why a secret scanning alert doesn't disappear just because the current file was edited, and why removing it from history would require a more disruptive operation.

---
