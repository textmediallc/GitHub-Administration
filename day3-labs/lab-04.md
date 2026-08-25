## Lab 4: Reviewing Dependency Changes on a Pull Request
**Real-World Scenario:** A teammate has opened a pull request that adds a new dependency to your project, and before approving it, you want to check whether that dependency introduces any known vulnerability.
**Why we are doing this:** Catching a vulnerable dependency during review, before it merges, is far cheaper than catching it afterward as a Dependabot alert.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Create a New Branch:** Click the branch dropdown, type `add-dependency`, and create the branch from `main`.
3. **Add a New Dependency:**
   * Open `package.json` on the new branch and add a new line inside `dependencies`, such as `"minimist": "1.2.5"` (an older version with a known advisory).
   * Commit directly to `add-dependency`.
4. **Open a Pull Request:** Click `Compare & pull request`, add a title, and click `Create pull request`.
5. **Open the Files Changed Tab:** Click `Files changed` and locate the dependency review panel, usually shown near the top of the diff for `package.json`.
6. **Review the Dependency Review Panel:** Confirm it lists `minimist` as newly added, along with its version.
7. **Check for a Vulnerability Flag:** Look for a warning icon or highlighted row indicating a known vulnerability in the added version.
8. **Click Into the Flagged Advisory:** If a vulnerability is flagged, click through to see its severity and the version that would resolve it.
9. **Update to a Safe Version:** Edit `package.json` again on the same branch, changing the version to a patched release (such as `1.2.6` or later), and commit.
10. **Confirm the Flag Clears:** Return to `Files changed` and confirm the dependency review panel no longer shows a vulnerability warning for `minimist`.
11. **Merge the Pull Request:** Once clean, merge the pull request into `main`.
12. **Verify:** Confirm you can explain where in the pull request UI dependency review appears, and why catching this before merge is preferable to catching it afterward as a Dependabot alert.

---
