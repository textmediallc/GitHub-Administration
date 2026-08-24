## Lab 21: Investigating History with Blame, Compare, and Revert in the Web UI
**Real-World Scenario:** A bug has appeared in production, and your team lead has asked you to figure out which change introduced it and undo it — using only the tools available on github.com, since you're triaging from a machine without your usual setup.
**Why we are doing this:** GitHub's web UI includes the same history-investigation tools most people reach for on the command line. Knowing them well means an administrator can respond to an incident from any browser, anywhere.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab`, which should have accumulated commits from several earlier labs.
2. **Review the Full Commit List:** Click `Commits` near the top of the file list to see every commit in chronological order.
3. **Open a Specific Commit:** Click on any commit message to view exactly what changed in that commit, with additions and deletions highlighted.
4. **Use Blame to Trace a Line's Origin:**
   * Open `README.md`, then click `Blame` in the top-right of the file view.
   * Confirm each line is annotated with the commit and author that last changed it.
   * *Explanation:* Blame view is the fastest way to answer "who changed this line, and in which commit" without leaving the browser.
5. **Jump from Blame to the Full Commit:** Click on any commit hash shown in the blame view to open the full commit details.
6. **Compare Two Points in History:**
   * In your browser's address bar, note the repository URL, then navigate to `github.com/your-username/team-service-lab/compare/main...HEAD~3` (adjust the range as needed) to see a cumulative diff across multiple commits.
   * Alternatively, use the branch dropdown's `Compare` option to select two specific branches or tags to compare.
7. **Identify a Commit to Revert:** From the commit list, choose any single commit you want to practice undoing.
8. **Open the Commit and Revert It:**
   * Open the commit's detail page.
   * If it was merged via a pull request, open that pull request and click the `Revert` button near the bottom.
   * If prompted, confirm creating a new pull request that reverts the change.
   * *Explanation:* `Revert` creates a brand-new commit that undoes a previous change, rather than erasing history — this keeps a clean, honest record of both the original change and the correction.
9. **Review the Revert Pull Request:** Click `Files changed` on the new revert pull request and confirm it exactly undoes the original commit.
10. **Merge the Revert:** Click `Merge pull request`, then `Confirm merge`.
11. **Confirm the Fix:** Return to the affected file and confirm its content now matches the state before the reverted commit.
12. **Verify:** Open `Insights > Network` one more time and confirm the revert commit and its originating pull request are clearly visible in the repository's history.

---
