## Lab 15: Administering Repository Settings and Collaborator Access
**Real-World Scenario:** You've been named the administrator for a new team repository. Before anyone starts committing code, you need to configure its settings and grant the right people the right level of access — entirely through the Settings UI.
**Why we are doing this:** Repository administration — feature toggles, merge rules, and access control — determines how a team is able to work together safely, and misconfiguration here causes real friction later.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab` and click `Settings`.
2. **Review Feature Toggles:**
   * Under `General > Features`, review the checkboxes for `Issues`, `Projects`, `Wikis`, and `Discussions`.
   * Leave `Issues` and `Wikis` enabled; this repository will use both.
3. **Configure Merge Button Options:**
   * Scroll to `Pull Requests`.
   * Review the options for `Allow merge commits`, `Allow squash merging`, and `Allow rebase merging`.
   * Disable `Allow merge commits` and leave squash merging enabled.
   * *Explanation:* Restricting to squash merges keeps the commit history on `main` clean — each pull request becomes exactly one commit.
4. **Open the Collaborators Panel:** Click `Collaborators and teams` in the left sidebar.
5. **Add a Collaborator:**
   * Click `Add people`.
   * Enter a username, full name, or email address of someone you have permission to invite (this can be a second personal account, a classmate, or your instructor).
   * Select a permission level — choose `Write`.
   * Click `Add [username] to this repository`.
   * *Explanation:* `Write` access allows pushing and managing issues/pull requests but not changing repository settings — that requires `Admin`.
6. **Review Permission Levels:** Without changing it, open the dropdown of available permission levels (`Read`, `Triage`, `Write`, `Maintain`, `Admin`) and note what each tier unlocks.
7. **Confirm the Invitation:** If you have access to the invited account, accept the invitation from the notifications inbox; otherwise, note that it will appear as `Pending` until accepted.
8. **Set the Default Branch:** Under `General`, confirm the default branch is set to `main`.
9. **Review the Repository's Community Standards:**
   * Click `Insights`, then `Community`.
   * Review the checklist of recommended files (README, license, contributing guidelines, etc.) and note which are already satisfied.
10. **Verify:** Return to the repository's main `Settings` page and confirm your merge-button configuration and collaborator invitation are both saved correctly.

---
