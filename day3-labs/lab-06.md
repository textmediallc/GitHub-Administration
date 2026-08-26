## Lab 6: Testing Secret Scanning Push Protection
**Real-World Scenario:** Your organization wants to stop leaked credentials before they ever reach GitHub, not just detect them afterward, and you've been asked to test push protection firsthand.
**Why we are doing this:** Experiencing a push protection block directly — and knowing how to respond — is the fastest way to understand prevention versus detection.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Enable Push Protection:** Click `Settings`, then `Code security`, and enable `Push protection` under the secret scanning section.
3. **Attempt to Add a Secret via the Web Editor:**
   * Click `Add file`, then `Create new file`, and name it `config/blocked-test.env`.
   * Add both of the following lines (as with Lab 5, AWS credentials are only detected as a matched pair — a lone secret key won't trigger push protection):
     ```
     AWS_ACCESS_KEY_ID=AKIAIOSFODNN7EXAMPLE
     AWS_SECRET_ACCESS_KEY=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY
     ```
   * This is the same widely published AWS example pair used in Lab 5, safe for this exercise.
4. **Attempt to Commit:** Try to commit this file directly to `main`.
5. **Observe the Block:** Confirm GitHub blocks the commit and displays a message identifying the exact file, line, and secret type detected.
6. **Read the Block Message Carefully:** Note the specific guidance GitHub provides for resolving the block.
7. **Remove the Secret:** Delete both flagged lines from the file content in the editor.
8. **Commit Successfully:** Confirm the commit now goes through without the blocked content.
9. **Test the Bypass Option:**
   * Repeat steps 3-4 with the same fake credential.
   * This time, look for and select a bypass option (such as "This is a false positive" or "This is a test credential"), providing that reason.
10. **Confirm the Bypass Is Logged:** Navigate to your organization's `Audit log` and search for an entry related to the push protection bypass, confirming it recorded who bypassed it and when.
11. **Clean Up:** Delete `config/blocked-test.env` entirely once finished testing.
12. **Verify:** Confirm you can explain, in your own words, why push protection represents prevention rather than detection, and why a bypass should always require a documented reason.

---
