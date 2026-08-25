## Lab 10: Case Study — Onboarding a New Engineering Team
**Real-World Scenario:** A new three-person engineering pod is joining your organization on Monday. You have until then to make sure their access, team structure, and first project are ready to go — entirely through the GitHub web UI.
**Why we are doing this:** This capstone lab combines account fundamentals from Day 1 with organizations, teams, security settings, and the PR workflow from today — the same combination of skills a real onboarding task requires.

### Step-by-Step Instructions:
1. **Review the Scenario:** You are onboarding a new team called `platform` into the organization created in Lab 5. They will own a new repository and need working access from day one.
2. **Create the Team:**
   * Navigate to your organization's `Teams` tab and click `New team`.
   * Name it `platform`, add a short description, and click `Create team`.
3. **Create the Team's Repository:**
   * Click the `+` icon, select `New repository`, and choose your organization as the owner.
   * Name it `platform-service`, set it `Public`, and check `Add a README file`, a `.gitignore`, and a license.
   * Click `Create repository`.
4. **Grant the Team Access:**
   * Open the `platform` team, click `Repositories`, then `Add repository`.
   * Select `platform-service` and set the permission level to `Write`.
5. **Configure Branch Protection:**
   * On `platform-service`, go to `Settings > Branches` and add a protection rule for `main` requiring a pull request and at least one approval.
6. **Add a CODEOWNERS File:**
   * Click `Add file`, then `Create new file`, and name it `.github/CODEOWNERS`.
   * Add the line `*  @your-org-name/platform` (replacing with your actual organization and team name).
   * Commit directly to `main`.
7. **Enable Required Review from Code Owners:**
   * Return to `Settings > Branches`, edit the protection rule for `main`, and check `Require review from Code Owners`.
8. **Add the New Team Members:**
   * Open the `platform` team's `Members` tab and click `Add a member`.
   * Add your own account (representing one of the three new hires, for this exercise), assigning the `Maintainer` role for the team if prompted.
9. **Set Up Initial Planning:**
   * Create a milestone on `platform-service` called `Sprint 1`.
   * Create two issues — "Set up project scaffolding" and "Write architecture overview" — both assigned to `Sprint 1` and labeled appropriately.
10. **Simulate the First Contribution:**
    * Create a branch named `feature/architecture-doc`.
    * Edit `README.md` on that branch to add a short `## Architecture` section, and commit.
    * Open a pull request, review and approve it (since you're the code owner), and merge it using squash merge.
11. **Reference and Close an Issue:** In the pull request description before merging (or in a follow-up commit), include `Closes #` followed by the "Write architecture overview" issue's number, and confirm it closes automatically once merged.
12. **Audit Your Own Work:**
    * Open the organization's `Audit log` and filter to `actor:your-username`.
    * Confirm you can see a clear record of the team creation, repository creation, permission grant, and merge — exactly the kind of evidence Case Study 4 discussed needing during a compliance review.
13. **Verify:** Confirm the `platform` team has working `Write` access to `platform-service`, branch protection with required code owner review is active, `Sprint 1` shows accurate progress, and the audit log gives a complete, readable record of everything you just configured.

---
