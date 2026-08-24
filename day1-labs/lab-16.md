## Lab 16: Forking a Repository and Contributing Entirely Through the Web Editor
**Real-World Scenario:** Your team relies on a small open-source utility, and you've found a typo in its README. You want to fix it and propose the change back — all without ever leaving your browser.
**Why we are doing this:** Forking is the standard mechanism for contributing to a project you don't have direct write access to, and GitHub's browser-based editor makes the entire fork-branch-propose workflow possible without a local clone.

### Step-by-Step Instructions:
1. **Find a Repository to Fork:** In your browser, go to `github.com/octocat/Spoon-Knife`, a small public repository GitHub maintains specifically for practicing this workflow.
2. **Fork the Repository:** Click the `Fork` button near the top-right of the page, and confirm the fork under your own account.
3. **Open a File in Your Fork:** On your forked copy, click into `README.md`.
4. **Edit the File in the Browser:** Click the pencil (edit) icon in the top-right of the file view.
5. **Make a Small Change:** Add a short, clearly harmless sentence to the file, since this is a shared public practice repository.
6. **Propose the Change as a New Branch:**
   * Scroll down to the commit panel.
   * Notice the option has changed to `Create a new branch for this commit and start a pull request`, since you're editing a file on a fork.
   * Enter a branch name such as `fix/readme-update`, and click `Propose changes`.
   * *Explanation:* Editing a file directly on a fork automatically offers this branch-and-PR path — no local clone or terminal is required to propose a change.
7. **Review the Compare View:** GitHub will now show a comparison between your new branch and the original repository's default branch, with your change highlighted.
8. **Start the Pull Request:** Click `Create pull request`, add a short title and description explaining the fix, and click `Create pull request` again.
9. **Review Your Open Pull Request:** Click the `Files changed` tab on your new pull request to confirm exactly the change you intended is included, and nothing else.
10. **Close Without Merging:** Since this is a shared public practice repository, scroll to the bottom of the pull request and click `Close pull request` rather than merging it.
    * *Explanation:* In a real contribution to an actual dependency, you would leave the pull request open for the maintainers to review; here, closing it keeps the shared practice repository clean for other students.
11. **Verify:** Navigate to your fork's `Pull requests` tab (filtered to `Closed`) and confirm your pull request appears with its full history intact.

---
