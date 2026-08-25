## Lab 8: Enabling Code Scanning with Default Setup
**Real-World Scenario:** None of your repositories currently have any automated code-level vulnerability scanning, and you've been asked to turn it on for the first time using the simplest available option.
**Why we are doing this:** Default setup is the right starting point for the overwhelming majority of repositories, and every administrator should know how to enable it in under a minute.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Open Code Security Settings:** Click `Settings`, then `Code security`.
3. **Locate Code Scanning:** Find the `Code scanning` section and click `Set up`, then choose `Default`.
4. **Review the Detected Configuration:** Read the summary GitHub shows of which languages it detected and which query suite it will use.
5. **Confirm Enablement:** Click `Enable CodeQL` (or the equivalent confirmation button) to finish setup.
6. **Check the Actions Tab:** Click the `Actions` tab and confirm a new workflow run has started, generated automatically by default setup.
7. **Wait for Completion:** Allow the run to finish (this may take a few minutes), then open it to confirm it completed successfully.
8. **Review the Security Tab:** Click `Security`, then `Code scanning`, and confirm the page now shows either a clean result or a list of findings.
9. **Confirm the Configuration Persisted:** Return to `Settings > Code security` and confirm code scanning now shows as `Enabled` via default setup, without any workflow file visible in your repository's files (since GitHub manages it behind the scenes).
10. **Verify:** Confirm you can explain why no `.github/workflows/` file appears in your repository despite code scanning actively running — this is the defining characteristic of default setup versus advanced setup.

---
