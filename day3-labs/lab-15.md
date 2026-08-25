## Lab 15: Running a Tabletop Incident Response Exercise
**Real-World Scenario:** Secret scanning has just alerted you to what looks like an active, currently-valid credential committed to one of your repositories, and you need to respond immediately and correctly.
**Why we are doing this:** Practicing the full detect-revoke-remediate sequence yourself, even in a simulated exercise, is what makes the response automatic under real pressure rather than something you have to look up mid-incident.

### Step-by-Step Instructions:
1. **Set Up the Simulated Incident:**
   * On `org-service-lab`, create a new file named `config/leaked.env`.
   * Add a line such as `STRIPE_SECRET_KEY=sk_live_51ExampleNotARealKeyForTraining0000` and commit directly to `main` (bypassing push protection with a documented reason if it blocks you, since this is a controlled exercise).
2. **Detect:**
   * Navigate to `Security > Secret scanning alerts` and confirm the alert for this credential appears.
   * Note the timestamp of detection.
3. **Assess Validity:** Check whether GitHub's validity check indicates this key as active (in this training exercise, it will correctly show as inactive, since it's not a real key — note this distinction for the write-up).
4. **Simulate Revocation:** Write a short note, as if this were real, describing the exact steps you would take with Stripe's own dashboard to revoke and rotate this specific key, even though you won't actually do so in this exercise.
5. **Remediate — Remove from the Current File:**
   * Edit `config/leaked.env`, remove the line containing the fake key, and commit.
6. **Remediate — Consider History:** Write a short note explaining that, in a real incident, this secret would still exist in the commit history and would require a history rewrite (such as using GitHub's file removal tools or contacting GitHub Support for full purge from caches) to be fully removed, since this lab will not perform that disruptive step.
7. **Investigate Usage:** Write a short note describing where, in a real scenario, you would check Stripe's own access logs for evidence the exposed key was used by an unauthorized party during the exposure window.
8. **Document the Incident:** Using the exercise, write a short incident summary covering: what was detected, when, how it was contained, what was rotated, and what if anything should change to prevent a recurrence.
9. **Write the Leadership Summary:** Condense your incident summary into two or three plain-language sentences suitable for a non-technical stakeholder, avoiding unnecessary alarm while still being accurate.
10. **Check the Audit Log:** Open your organization's `Audit log` and confirm you can locate the relevant events (the commit, the alert, the dismissal or resolution) tied to this exercise.
11. **Clean Up:** Confirm `config/leaked.env` no longer contains any credential-like content in the current version of the file.
12. **Verify:** Confirm your written incident summary follows the detect-revoke-remediate structure explicitly, with revocation clearly prioritized ahead of any cleanup work — exactly the sequencing this week's material emphasized.

---
