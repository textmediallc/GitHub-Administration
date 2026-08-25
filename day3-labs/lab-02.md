## Lab 2: Triaging a Dependabot Alert and Applying a Security Update
**Real-World Scenario:** Dependabot has just generated an alert on one of your repositories for a dependency with a known, published vulnerability, and you need to review, understand, and resolve it.
**Why we are doing this:** Reviewing and resolving a real Dependabot alert — not just reading about the process — is a core, recurring task for any GitHub administrator.

### Step-by-Step Instructions:
1. **Confirm a Vulnerable Dependency Exists:** On `org-service-lab`, open `package.json` and confirm it lists a known-outdated package such as `"lodash": "4.17.11"` (an older version with published advisories). If not already present, add it and commit directly to `main`.
2. **Wait for or Trigger the Alert:** Navigate to `Security` tab, then `Dependabot alerts`. If no alert has appeared yet, wait a few minutes and refresh, since GitHub's scan runs shortly after the manifest changes.
3. **Open the Alert:** Click into the specific alert listed for your vulnerable package.
4. **Review the Detail:** Note the severity badge, the vulnerable version range, and the patched version GitHub recommends.
5. **Check for an Automated Fix:** Look for a note indicating Dependabot has opened, or can open, a pull request with the fix.
6. **Trigger the Fix (If Not Automatic):** If no pull request exists yet, click `Create Dependabot security update` if that option is available on the alert.
7. **Review the Generated Pull Request:** Navigate to `Pull requests` and open the one Dependabot created, reviewing its `Files changed` tab to confirm it only touches the manifest and lock file.
8. **Merge the Fix:** Approve and merge the pull request using your repository's configured merge strategy.
9. **Confirm the Alert Closes:** Return to `Security > Dependabot alerts` and confirm the alert you resolved now shows as closed.
10. **Verify:** Confirm you can point to the exact version number the fix updated to, and explain why the alert closed automatically rather than requiring a manual dismissal.

---
