## Lab 9: Provisioning a New Team Repository and Configuring Its Initial Settings
**Real-World Scenario:** Your team is kicking off a new internal service and you've been asked to set up the repository from scratch, following the same conventions used across the rest of the organization's projects — and hand it off to developers ready to go.
**Why we are doing this:** Correctly provisioning a repository from day one — with the right visibility, ignore rules, and license — avoids painful cleanup later and sets a consistent standard for the team. As the administrator, your job is to configure the repository correctly and hand off a working clone URL; the developers on your team will be the ones cloning it locally.

### Step-by-Step Instructions:
1. **Create the Repository:**
   * On `github.com`, click the `+` icon and select `New repository`.
   * Name it `team-service-lab`.
2. **Set Visibility:** Choose `Public` for this exercise (in a real workplace, this would typically be `Private`).
3. **Initialize the Repository:**
   * Check `Add a README file`.
   * Under `Add .gitignore`, select a template matching a language your team uses.
   * Under `Choose a license`, select a license template.
   * *Explanation:* Initializing with these three files at creation time avoids several manual setup steps later and establishes clear legal terms immediately.
4. **Create the Repository:** Click `Create repository`.
5. **Confirm the Initial Files:** Confirm `README.md`, `.gitignore`, and `LICENSE` are all present in the file list.
6. **Add a Project Notes File:**
   * Click `Add file`, then `Create new file`.
   * Name it `NOTES.md` and add a single line of text.
   * Commit directly to `main`.
7. **Review the Clone URL:**
   * Click the green `Code` button and review both the `HTTPS` and `SSH` tabs.
   * *Explanation:* This is the URL you would hand off to your development team — as the administrator, provisioning the repository correctly and sharing this URL completes your part of the task; you don't need to clone it yourself to verify it works.
8. **Set the Default Branch:** Under `Settings > General`, confirm the default branch is listed as `main`.
9. **Review Repository Visibility:** Under `Settings > General`, confirm the visibility badge matches what you selected at creation.
10. **Verify:** Confirm the repository homepage shows `README.md`, `.gitignore`, `LICENSE`, and `NOTES.md`, and that you can locate both clone URL formats from the `Code` button.

---
