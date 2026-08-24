## Lab 13: Managing Files Directly on GitHub — Add, Edit, Delete, and Track History in the Browser
**Real-World Scenario:** A teammate spots a typo in a configuration file and pings you to fix it right away. You're on a shared machine with only browser access — no local clone, no terminal.
**Why we are doing this:** Administrators frequently make or review small file changes without ever touching a local copy of the repository. Being fluent in the browser-based file editor is a core, everyday skill.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab` on `github.com`.
2. **Edit an Existing File:**
   * Click on `README.md` in the file list, then click the pencil (edit) icon in the top-right of the file view.
   * Make a small text change.
3. **Preview Your Change:** Click the `Preview` tab above the editor to confirm the Markdown renders as expected before committing.
4. **Commit Directly to main:**
   * Scroll down to the `Commit changes` panel.
   * Write a clear commit message describing the fix.
   * Select `Commit directly to the main branch`, then click `Commit changes`.
5. **Add a New File:**
   * Click `Add file`, then `Create new file`.
   * Name it `CHANGELOG.md` and add a single line of text.
   * Commit directly to `main`.
6. **Edit the New File Again:**
   * Open `CHANGELOG.md` and click the pencil icon.
   * Add a second line of text and commit directly to `main` again.
7. **Delete a File:**
   * Open any file you no longer need (or create a throwaway file first, named `temp.md`, to safely delete).
   * Click the trash can icon in the top-right of the file view.
   * Write a commit message explaining the deletion and commit directly to `main`.
8. **Review the File History:**
   * Open `CHANGELOG.md` and click `History` in the top-right corner of the file view.
   * Confirm both edits appear as separate entries, each with its own commit message and timestamp.
9. **Compare Two Versions of a File:**
   * From the file history list, click on the older commit, then use GitHub's comparison view (click the commit hash, then look for the file's diff) to see exactly what changed between versions.
10. **Review the Full Commit List:** Click `Commits` near the top of the repository's file list and confirm all of today's changes appear in order with clear messages.
11. **Verify:** Confirm the repository's homepage reflects the final state — `CHANGELOG.md` present with two lines, `temp.md` absent, and `README.md` showing your edited text.

---
