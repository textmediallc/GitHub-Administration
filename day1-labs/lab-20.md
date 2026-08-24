## Lab 20: Enforcing Code Quality with Branch Protection, Required Reviews, and CODEOWNERS
**Real-World Scenario:** Your team is preparing for its first official release, and leadership has asked that no change reach `main` without a review from someone on the right team — and that the right reviewer be requested automatically.
**Why we are doing this:** Branch protection rules and a CODEOWNERS file are how administrators enforce review policy at the platform level, rather than relying on everyone remembering to ask for review manually.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab`.
2. **Create a CODEOWNERS File:**
   * Click `Add file`, then `Create new file`.
   * Name it `.github/CODEOWNERS` (typing the `/` will automatically create the `.github` folder).
   * Add a line such as `*  @your-username`, which designates you as the owner of every file in the repository.
   * *Explanation:* CODEOWNERS maps file paths to specific people or teams, so GitHub knows exactly who to request review from when a matching file changes.
3. **Commit the File:** Commit directly to `main` with a clear message.
4. **Open Branch Settings:** Click `Settings`, then `Branches` in the left sidebar.
5. **Add a Branch Protection Rule:**
   * Click `Add branch protection rule`.
   * In the branch name pattern field, enter `main`.
6. **Require Pull Requests:**
   * Check `Require a pull request before merging`.
   * Check `Require approvals` and set the required number of approvals to `1`.
7. **Require Review from Code Owners:**
   * Check `Require review from Code Owners`.
   * *Explanation:* This setting connects the CODEOWNERS file to branch protection — a pull request touching a file you own cannot be merged without your approval.
8. **Save the Rule:** Click `Create` to save the branch protection rule.
9. **Test the Rule with a Web Edit:**
   * Open `README.md`, click the pencil icon, and make a small change.
   * In the commit panel, select `Create a new branch for this commit and start a pull request`, name the branch `test/branch-protection`, and click `Propose changes`.
10. **Open the Pull Request:** Click `Create pull request` on the resulting compare page.
11. **Confirm the Review Requirement:** On the new pull request, confirm GitHub shows a message that review is required before merging, and that the `Merge pull request` button is disabled until that review is submitted.
12. **Approve and Merge:** Since you are the designated code owner, click `Files changed`, then `Review changes`, select `Approve`, and submit the review. Return to the `Conversation` tab and confirm the `Merge pull request` button is now enabled.
13. **Verify:** Attempt to edit a file directly on `main` again and confirm GitHub now routes the change through the same branch-and-pull-request flow rather than allowing a direct commit.

---
