## Lab 3: Configuring Dependabot Version Updates with dependabot.yml
**Real-World Scenario:** Your team wants dependencies kept broadly current on an ongoing basis, not just patched reactively whenever a vulnerability is found.
**Why we are doing this:** Committing a working `dependabot.yml` file is the only way to enable proactive version updates, and it's a file every well-maintained repository should have.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Create the Dependabot Config File:**
   * Click `Add file`, then `Create new file`.
   * Name it `.github/dependabot.yml`.
3. **Write the Configuration:** Enter the following YAML:
   ```
   version: 2
   updates:
     - package-ecosystem: "npm"
       directory: "/"
       schedule:
         interval: "weekly"
       open-pull-requests-limit: 5
   ```
4. **Commit the File:** Commit directly to `main` with a message such as "Add Dependabot version update configuration".
5. **Confirm Dependabot Recognizes the File:** Navigate to `Insights > Dependency graph > Dependabot`, and confirm your configuration is listed with its schedule.
6. **Trigger a Manual Check:** On the same `Dependabot` tab, look for a `Last checked` timestamp and, if available, a way to manually trigger a check now rather than waiting for the weekly schedule.
7. **Review Any Generated Pull Requests:** Check `Pull requests` for any version-update PRs Dependabot has opened, distinct from any earlier security-update PR from Lab 2.
8. **Add a Second Ecosystem Entry:**
   * Edit `dependabot.yml` again and add a second `package-ecosystem: "github-actions"` block monitoring `.github/workflows`.
   * Commit the change.
9. **Confirm Both Ecosystems Are Tracked:** Return to `Dependabot` under the Dependency graph tab and confirm both `npm` and `github-actions` now appear as monitored ecosystems.
10. **Verify:** Confirm you can explain the difference between what you configured in this lab and the automatic security update from Lab 2, without looking back at the slides.

---
