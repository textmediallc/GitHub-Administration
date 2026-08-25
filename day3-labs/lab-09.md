## Lab 9: Configuring Code Scanning with a Custom CodeQL Workflow (Advanced Setup)
**Real-World Scenario:** Your team's build process is more complex than default setup can automatically handle, and you've been asked to configure code scanning manually instead.
**Why we are doing this:** Understanding advanced setup — and being able to read or write the underlying workflow file — matters for any repository whose needs go beyond default setup's automatic detection.

### Step-by-Step Instructions:
1. **Open a Different Repository:** Navigate to `platform-service` (or another repository without code scanning already enabled via default setup).
2. **Create the Workflow File:**
   * Click `Add file`, then `Create new file`.
   * Name it `.github/workflows/codeql.yml`.
3. **Write the Workflow:** Enter the following YAML:
   ```
   name: CodeQL Analysis

   on:
     push:
       branches: [main]
     pull_request:
       branches: [main]
     schedule:
       - cron: "0 6 * * 1"

   jobs:
     analyze:
       runs-on: ubuntu-latest
       permissions:
         security-events: write
       steps:
         - name: Checkout repository
           uses: actions/checkout@v4
         - name: Initialize CodeQL
           uses: github/codeql-action/init@v3
           with:
             languages: javascript
         - name: Perform CodeQL Analysis
           uses: github/codeql-action/analyze@v3
   ```
4. **Commit the Workflow:** Commit directly to `main` with a message such as "Add advanced CodeQL workflow".
5. **Confirm It Runs:** Click the `Actions` tab and confirm a new `CodeQL Analysis` run has started.
6. **Review the Run:** Open the run and confirm both the `Initialize CodeQL` and `Perform CodeQL Analysis` steps complete successfully.
7. **Check the Security Tab:** Once complete, click `Security`, then `Code scanning`, and confirm results now appear, sourced from your custom workflow this time.
8. **Confirm the Setting Reflects Advanced Setup:** Navigate to `Settings > Code security` and confirm code scanning shows as configured via a workflow file rather than default setup.
9. **Modify the Schedule:** Edit the workflow file, changing the cron schedule to run weekly on a different day, and commit the change.
10. **Verify the Change Took Effect:** Confirm the updated schedule is reflected the next time the Actions tab shows the workflow's trigger configuration.
11. **Verify:** Confirm you can explain at least one concrete reason a team might choose advanced setup over default setup, based on what you configured in this lab.

---
