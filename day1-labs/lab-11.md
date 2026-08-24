## Lab 11: Branching and Tagging a Release Through the Web UI
**Real-World Scenario:** Your team is preparing its first official release. A small change needs to go through a branch and pull request rather than straight to `main`, and once it's merged, the release needs to be marked with a version tag so it can always be found again.
**Why we are doing this:** Branches and tags are two of the most fundamental tools for managing change safely — branches isolate work in progress, and tags mark a fixed, permanent point in history. Both can be created and managed entirely from the web UI.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab` from Lab 9.
2. **Create a New Branch:**
   * Click the branch dropdown (it will show `main`).
   * Type a new branch name, `feature/web-ui-branch`, and select `Create branch: feature/web-ui-branch from 'main'`.
3. **Confirm You're on the New Branch:** Check the branch dropdown now shows `feature/web-ui-branch` as the active branch.
4. **Make a Change on the Branch:**
   * Open `NOTES.md`, click the pencil icon, and add a new line of text.
   * In the commit panel, confirm it is set to `Commit directly to the feature/web-ui-branch branch`, and click `Commit changes`.
5. **Open the Pull Request Banner:** Return to the repository's main page and click the `Compare & pull request` banner that GitHub displays for your recently pushed branch.
6. **Create the Pull Request:** Confirm the base branch is `main` and the compare branch is `feature/web-ui-branch`, add a short title and description, and click `Create pull request`.
7. **Review the Changes:** Click the `Files changed` tab and confirm only your intended edit appears.
8. **Merge the Pull Request:** Click `Merge pull request`, then `Confirm merge`.
9. **Delete the Merged Branch:** Click `Delete branch` on the confirmation screen.
   * *Explanation:* Once a branch's changes are merged, deleting it keeps the branch list clean — GitHub even surfaces the button right where you need it.
10. **Draft a New Release:**
    * Click `Releases` in the right sidebar of the repository homepage (or the `Code` tab, then `Releases`).
    * Click `Draft a new release`.
11. **Create a New Tag:**
    * In the `Choose a tag` field, type `v1.0.0` and select `Create new tag: v1.0.0 on publish`.
    * *Explanation:* Unlike a branch, a tag marks a fixed point in history and never moves forward — ideal for marking exactly what code shipped in a release.
12. **Publish the Release:** Add a release title and short notes summarizing the change, then click `Publish release`.
13. **Verify:** Confirm `v1.0.0` appears under the repository's `Tags`, the release appears under `Releases` with your notes, `feature/web-ui-branch` no longer appears in the branch list, and the `Insights > Network` graph shows where the branch merged into `main`.

---
