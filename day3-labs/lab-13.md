## Lab 13: Enabling Security Configurations Across Multiple Repositories
**Real-World Scenario:** Manually enabling Dependabot, secret scanning, and push protection on every single repository individually doesn't scale, and you've been asked to set up a reusable baseline instead.
**Why we are doing this:** Security configurations are what make a secure baseline achievable across dozens of repositories, rather than depending on someone remembering every setting each time.

### Step-by-Step Instructions:
1. **Open Your Organization:** Navigate to your organization, then `Settings`, then `Code security`.
2. **Open Security Configurations:** Click `Configurations` in the left sidebar (or the equivalent security configurations page).
3. **Review the Recommended Configuration:** Open GitHub's built-in recommended configuration and review which features it enables by default.
4. **Create a New Configuration:** Click `New configuration`.
5. **Name It:** Enter a name such as "Baseline Security Standard".
6. **Enable Core Features:** Turn on Dependency graph, Dependabot alerts, Dependabot security updates, Secret scanning, and Secret scanning push protection.
7. **Set Enforcement Level:** For push protection specifically, set it to `Enforced` rather than merely `Enabled`, if that distinction is available.
8. **Save the Configuration:** Click `Save configuration` (or equivalent) to finish creating it.
9. **Apply to Existing Repositories:**
   * From the configuration's detail page, click `Apply to repositories`.
   * Select `org-service-lab` and `platform-service`, and apply the configuration.
10. **Set as Default for New Repositories:** Find the option to set this configuration as the default applied automatically to any newly created repository in the organization, and enable it.
11. **Verify Application:** Return to the configurations list and confirm both repositories now show as matching the "Baseline Security Standard" configuration.
12. **Verify:** Confirm you can explain what happens differently for a brand-new repository created in this organization from now on, compared to before this lab.

---
