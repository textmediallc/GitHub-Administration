## Lab 1: Exploring the Dependency Graph and Exporting an SBOM
**Real-World Scenario:** A vendor security questionnaire has asked your team to provide a complete inventory of every open-source component used in one of your applications, including indirect dependencies you may not even be aware of.
**Why we are doing this:** Understanding what the dependency graph actually detects — and how to export it as a formal SBOM — is the starting point for every other security feature covered this week.

### Step-by-Step Instructions:
1. **Open a Repository with Dependencies:** Navigate to `org-service-lab` (or another repository from an earlier lab that has a manifest file such as `package.json`). If none of your existing repositories has one, create a new file named `package.json` with the content `{"name": "demo-app", "version": "1.0.0", "dependencies": {"lodash": "4.17.11"}}` and commit it directly to `main`.
2. **Open the Dependency Graph:** Click `Insights`, then `Dependency graph` in the left sidebar.
3. **Review Detected Dependencies:** Confirm `lodash` (or whichever packages your manifest lists) appears under the `Dependencies` tab.
4. **Check Repository Security Settings:** Click `Settings`, then `Code security`, and confirm `Dependency graph` shows as enabled.
5. **Enable Dependabot Alerts:** On the same page, find `Dependabot alerts` and click `Enable`.
6. **Return to the Dependency Graph:** Click back to `Insights > Dependency graph` and note whether any of your listed dependencies now show a vulnerability warning icon.
7. **Export an SBOM:**
   * While still on the `Dependency graph` page, click `Export SBOM` in the top-right corner.
   * Confirm a JSON file downloads to your computer.
8. **Inspect the SBOM:** Open the downloaded file in a text editor (or view it directly if your browser supports it) and locate the `packages` section, confirming your dependency is listed with its name and version.
9. **Note the Format:** Confirm the file's `spdxVersion` field is present, identifying this as a standard SPDX-format document.
10. **Verify:** Confirm you can explain, in your own words, the difference between a direct and a transitive dependency, and why an SBOM needs to be regenerated periodically rather than treated as a one-time export.

---
