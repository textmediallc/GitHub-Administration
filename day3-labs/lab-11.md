## Lab 11: Publishing a Security Advisory
**Real-World Scenario:** A vulnerability has been identified in one of your repositories, and rather than just fixing it silently, you need to responsibly document and eventually disclose it.
**Why we are doing this:** Walking through an advisory's full private-draft-to-public lifecycle is the only way to really understand the process, not just the concept.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Start a New Draft Advisory:** Click `Security`, then `Advisories`, then `New draft security advisory`.
3. **Fill in the Title:** Enter a descriptive title, such as "Insecure default configuration allows unauthorized read access".
4. **Set the Severity:** Choose a severity level, such as `Medium`, and note the CVSS score fields available.
5. **Write the Description:** In the description field, explain the vulnerability in a few sentences: what it is, how it could be exploited, and its potential impact.
6. **Identify the Affected Product:** Add an affected product entry, specifying this repository's package name (or a placeholder name) and the vulnerable version range, such as `< 1.0.1`.
7. **Add a Patched Version:** Specify the version that resolves the issue, such as `1.0.1`.
8. **Add a Temporary Collaborator (If Available):** If you have a second account or classmate available, add them as a temporary collaborator on the draft; otherwise, skip this step and note where the option lives.
9. **Create a Fixing Pull Request:**
   * Make a small, real change to a file in your repository representing the fix (such as updating a configuration default).
   * Open a pull request for this change.
10. **Link the Pull Request:** Return to the draft advisory and link the pull request you just opened as the fix.
11. **Merge the Fix:** Approve and merge the linked pull request.
12. **Publish the Advisory:** Return to the advisory and click `Publish advisory`.
13. **Verify:** Confirm the published advisory is now visible under your repository's `Security > Advisories` tab, and that you can explain why publishing before merging the fix would have been the wrong order of operations.

---
