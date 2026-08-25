## Lab 4: Securing a Workflow with Encrypted Secrets
**Real-World Scenario:** The workflow from the previous lab now needs to call a fictional internal API, and doing so requires an API key. That key must never appear in plain text in the repository or in a workflow log.
**Why we are doing this:** Knowing how to store and correctly reference a secret is essential any time a workflow needs to authenticate to something — and misconfiguring this is one of the most common ways credentials leak.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab`.
2. **Open Secrets Settings:** Click `Settings`, then `Secrets and variables`, then `Actions`.
3. **Add a Repository Secret:**
   * Click `New repository secret`.
   * Name it `DEMO_API_KEY`.
   * In the value field, enter a placeholder value such as `demo-key-12345`.
   * Click `Add secret`.
4. **Confirm the Secret Is Listed:** Verify `DEMO_API_KEY` now appears in the secrets list, with its value hidden.
5. **Edit Your Workflow File:**
   * Navigate to `.github/workflows/hello-actions.yml` and click the pencil icon.
6. **Reference the Secret:** Add a new step at the end of the `steps:` list:
   ```
         - name: Use the demo API key
           run: echo "The key starts with ${DEMO_API_KEY:0:4}..."
           env:
             DEMO_API_KEY: ${{ secrets.DEMO_API_KEY }}
   ```
7. **Commit the Change:** Commit directly to `main` with a message such as "Reference DEMO_API_KEY secret in workflow".
8. **Run the Workflow:** Go to the `Actions` tab, select `Hello Actions`, click `Run workflow`, and confirm it manually.
9. **Inspect the Log:**
   * Open the completed run and expand the `Use the demo API key` step.
   * Confirm only the first four characters are visible, exactly as the command intended.
10. **Test GitHub's Redaction:**
    * Edit the workflow again and temporarily change the step to `run: echo "The full key is $DEMO_API_KEY"`.
    * Commit and run the workflow again.
    * Open the log and confirm GitHub automatically masks the secret value with `***` even though the command tried to print it in full.
    * *Explanation:* GitHub scans log output for any exact match to a known secret value and redacts it automatically, regardless of how a step tries to use it — a safety net, not a replacement for careful workflow design.
11. **Clean Up:** Edit the workflow one more time to remove the full-print line, leaving only the safe, partial-print version, and commit.
12. **Verify:** Confirm the secret's value never appears in full anywhere in the run log, and that you can explain the difference between a repository secret and an organization secret.

---
