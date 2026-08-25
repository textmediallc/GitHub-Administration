## Lab 8: Running a Full Pull Request Review Workflow
**Real-World Scenario:** Your organization has decided that no change should reach `main` without at least one review — and you've been asked to prove the process actually works end to end, not just that the setting is turned on.
**Why we are doing this:** Running a complete pull request from open to merge — including a rejection and a fix — is the daily workflow every contributor and reviewer on a real team goes through constantly.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Enable Branch Protection:**
   * Click `Settings`, then `Branches`.
   * Click `Add branch protection rule`, enter `main` as the pattern.
   * Check `Require a pull request before merging` and `Require approvals` (set to `1`), then click `Create`.
3. **Create a New Branch:**
   * Click the branch dropdown, type `feature/add-status-section`, and select `Create branch: feature/add-status-section from 'main'`.
4. **Make a Change:**
   * Open `README.md` on the new branch, click the pencil icon, and add a `## Status` section with one line of text.
   * Commit directly to `feature/add-status-section`.
5. **Open a Pull Request:** Click the `Compare & pull request` banner, add a title and description, and click `Create pull request`.
6. **Request a Review (If Available):** If you have a second account or a classmate available, click the gear icon next to `Reviewers` and request their review; otherwise, proceed as the sole reviewer for this exercise.
7. **Leave a Review Comment:**
   * Click `Files changed`.
   * Click the `+` icon next to a line in your diff and leave a comment asking a clarifying question.
   * Submit the comment as part of a `Comment` review (not yet an approval).
8. **Confirm the Merge Button Is Blocked:** Return to the `Conversation` tab and confirm GitHub shows that a review is still required before merging.
9. **Submit an Approving Review:**
   * Click `Files changed`, then `Review changes`.
   * Select `Approve` and submit.
10. **Merge the Pull Request:** Return to `Conversation`, confirm `Merge pull request` is now enabled, click it, then `Confirm merge`.
11. **Delete the Branch:** Click `Delete branch` on the confirmation screen.
12. **Verify:** Confirm `README.md` on `main` now shows your `## Status` section, and that the merged pull request's `Conversation` tab shows a clear record of the comment, the approval, and the merge.

---
