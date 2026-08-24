## Lab 14: Archiving, Restoring, and Exploring Ownership Controls
**Real-World Scenario:** A project your team maintained for over a year has just been formally deprecated. Leadership wants the code preserved for reference, but no one should be able to accidentally change it going forward.
**Why we are doing this:** Knowing how to safely retire a repository through the Settings UI — and how to reverse that decision if plans change — is a core repository administration responsibility.

### Step-by-Step Instructions:
1. **Create a Practice Repository:**
   * Click the `+` icon and select `New repository`.
   * Name it `deprecated-service-lab`, set it to `Public`, and check `Add a README file`.
   * Click `Create repository`.
2. **Open Repository Settings:** Click the `Settings` tab.
3. **Locate the Danger Zone:** Scroll to the bottom of the `General` settings page.
4. **Review the Available Actions:** Without clicking anything yet, read through the options listed: changing visibility, transferring ownership, archiving, and deleting.
   * *Explanation:* These are grouped together because each one is high-impact and, in the case of deletion, difficult or impossible to reverse — GitHub deliberately makes you slow down here.
5. **Archive the Repository:**
   * Click `Archive this repository`.
   * Read the confirmation dialog carefully, type the repository name if prompted, and confirm.
6. **Confirm Read-Only Status:**
   * Notice the `Archived` badge now displayed near the repository name at the top of the page.
   * Click into `README.md` and confirm the pencil (edit) icon is no longer available.
   * Click `Issues` and confirm the option to open a new issue is disabled.
7. **Unarchive the Repository:**
   * Return to `Settings > Danger Zone`.
   * Click `Unarchive this repository` and confirm.
8. **Confirm Read-Write Access Is Restored:**
   * Open `README.md` again and confirm the pencil (edit) icon has returned.
   * Confirm `Issues` now allows creating a new issue again.
9. **Review Transfer Ownership (Read-Only Exercise):**
   * Scroll to `Transfer ownership` in the Danger Zone and click it to view the form.
   * Read what information it requires (new owner's username and repository name confirmation) without submitting it.
   * *Explanation:* Transferring ownership moves a repository to a different account or organization while preserving its stars, forks, and history — useful when a project moves teams.
10. **Review Visibility Change (Read-Only Exercise):**
    * Scroll to `Change repository visibility` and click it to view what switching from `Public` to `Private` would require, without confirming.
11. **Verify:** Confirm you can explain the difference between archiving (reversible, read-only) and deleting (permanent) a repository, and where each action lives in the Settings UI.

---
