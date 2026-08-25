## Lab 12: Writing a Security Policy (SECURITY.md)
**Real-World Scenario:** A security researcher wants to responsibly report a finding on one of your repositories but has no idea how to reach your team, and you've been asked to fix that.
**Why we are doing this:** A clear, discoverable SECURITY.md file is a small effort with a real, practical payoff for how a project is perceived by the security community.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Create the File:** Click `Add file`, then `Create new file`, and name it `SECURITY.md`.
3. **Write a Title and Introduction:** Add a top-level heading such as `# Security Policy` and a short sentence describing the project's commitment to security.
4. **Add a Supported Versions Section:** Include a `## Supported Versions` heading with a short table or list noting which versions currently receive security updates.
5. **Add a Reporting Section:** Include a `## Reporting a Vulnerability` heading explaining exactly how to report an issue — for this exercise, reference GitHub's private vulnerability reporting feature.
6. **Enable Private Vulnerability Reporting:**
   * Click `Settings`, then `Code security`.
   * Find `Private vulnerability reporting` and click `Enable`.
7. **Set a Response Time Expectation:** Back in `SECURITY.md`, add a sentence setting an honest expectation, such as "We aim to acknowledge reports within 5 business days."
8. **Commit the File:** Commit directly to `main` with a message such as "Add security policy".
9. **Confirm GitHub Surfaces It:** Navigate to the repository's `Security` tab and confirm a `Security policy` link now appears, pointing to your new file.
10. **Test the Reporting Flow:** Click through to `Report a vulnerability` (enabled in step 6) and review the report form that appears, without submitting a real report.
11. **Verify:** Confirm you can explain why pointing to private vulnerability reporting is preferable to listing a plain email address, when that feature is available.

---
