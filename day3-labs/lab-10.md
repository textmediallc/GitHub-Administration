## Lab 10: Triaging and Resolving a Code Scanning Alert
**Real-World Scenario:** Your code scanning workflow from a previous lab has surfaced a real finding, and you need to review, understand, and resolve it the way a working developer would.
**Why we are doing this:** Reading a CodeQL alert's data-flow path and correctly resolving or dismissing it is a core skill for anyone maintaining code scanning across a real codebase.

### Step-by-Step Instructions:
1. **Introduce a Detectable Pattern:**
   * On `platform-service`, create a new file named `app.js`.
   * Add simple JavaScript code containing a common flagged pattern, such as: `const query = "SELECT * FROM users WHERE id = " + userInput; db.execute(query);`
   * Commit directly to `main`.
2. **Wait for the Scan:** Allow the CodeQL workflow from Lab 9 to run against this new commit (check the `Actions` tab for the run to complete).
3. **Open the Security Tab:** Click `Security`, then `Code scanning`, and look for a new alert related to your added code.
4. **Open the Alert:** Click into the alert to view its full detail.
5. **Review the Data-Flow Path:** If shown, review the steps CodeQL traces from where the untrasted input enters the code to where it's used unsafely.
6. **Read the Recommendation:** Note any guidance CodeQL provides about how to fix this class of issue (such as using parameterized queries).
7. **Fix the Code:**
   * Edit `app.js` to remove the unsafe string concatenation, replacing it with a comment noting a parameterized query would be used in production.
   * Commit the fix directly to `main`.
8. **Wait for Re-Scan:** Allow the workflow to run again against the fixed code.
9. **Confirm the Alert Closes:** Return to `Security > Code scanning` and confirm the alert is now marked as closed or resolved.
10. **Practice a Dismissal:** On any other open alert (or by reintroducing a test pattern), practice dismissing an alert with a specific reason, such as "used in tests," to see the dismissal flow.
11. **Verify:** Confirm you can describe the specific data-flow path CodeQL showed for your alert, in your own words, without re-reading the alert.

---
