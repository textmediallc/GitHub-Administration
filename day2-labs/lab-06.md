## Lab 6: Building Teams and Assigning Repository Permissions
**Real-World Scenario:** Your organization now has several repositories and a growing headcount. Instead of adding each person to each repository individually, you've been asked to set up a proper team structure.
**Why we are doing this:** Team-based access is the scalable permission pattern every real organization of any size relies on — this lab builds and tests that pattern directly.

### Step-by-Step Instructions:
1. **Open Your Organization:** Navigate to the organization created in Lab 5.
2. **Open the Teams Tab:** Click `Teams`, then `New team`.
3. **Create a Parent Team:**
   * Name it `engineering`.
   * Add a short description, and click `Create team`.
4. **Create a Child Team:**
   * Return to `Teams` and click `New team` again.
   * Name it `engineering/backend` (or select `engineering` as the parent team if prompted separately).
   * Click `Create team`.
   * *Explanation:* Nesting `backend` under `engineering` means members of `backend` are also considered part of the broader `engineering` team for mention and visibility purposes.
5. **Add Yourself to the Child Team:**
   * Open the `backend` team, click `Members`, then `Add a member`.
   * Add your own account (or a second test account, if available) and confirm.
6. **Grant the Team Repository Access:**
   * Open the `backend` team, click `Repositories`, then `Add repository`.
   * Select `org-service-lab` from Lab 5.
   * Set the permission level to `Write` and confirm.
7. **Verify Access from the Repository Side:**
   * Navigate to `org-service-lab`, click `Settings`, then `Collaborators and teams`.
   * Confirm `backend` is listed with `Write` access.
8. **Test the Access:**
   * As a member of `backend`, open `README.md` in `org-service-lab` and confirm the pencil (edit) icon is available, since `Write` access permits it.
9. **Change the Permission Level:**
   * Return to the `backend` team's `Repositories` tab.
   * Change the permission level on `org-service-lab` from `Write` to `Read`.
10. **Confirm the Change Took Effect:** Reopen `README.md` and confirm the edit icon is no longer available.
11. **Verify:** Confirm you can explain how changing a single team's permission level instantly affects every member of that team, without editing each person's access individually.

---
