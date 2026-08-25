## Lab 9: Planning Work with Issues, Milestones, and a Project Board
**Real-World Scenario:** Your team is about to start work on a small release and needs a shared view of what's planned, what's in progress, and what's done — without adopting a separate project management tool.
**Why we are doing this:** Issues, milestones, and project boards together are GitHub's native planning toolkit, and knowing how to set them up is a routine task for anyone administering a team's day-to-day workflow.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `org-service-lab`.
2. **Create a Milestone:**
   * Click `Issues`, then `Milestones`, then `New milestone`.
   * Title it `v1.0 Release`, set a due date a few weeks out, and click `Create milestone`.
3. **Create Three Issues:**
   * Click `New issue` and create three separate issues titled, for example, "Write onboarding docs," "Fix footer alignment," and "Add health check endpoint."
   * For each, assign it to the `v1.0 Release` milestone before submitting.
4. **Label the Issues:**
   * Open each issue and, using the `Labels` panel on the right, apply an appropriate existing label (such as `documentation` or `bug`), creating a new label if a suitable one doesn't exist.
5. **Check Milestone Progress:** Return to `Issues > Milestones` and confirm `v1.0 Release` shows 0% complete with all three issues listed as open.
6. **Create a Project:**
   * Click the `Projects` tab (at the organization or repository level) and click `New project`.
   * Choose the `Board` template and name it `v1.0 Planning`.
7. **Add Your Issues to the Board:**
   * Click `Add item`, and search for and add each of your three issues to the board.
8. **Organize the Board:**
   * Confirm the default columns (such as `Todo`, `In Progress`, `Done`).
   * Drag one issue into `In Progress` to represent work that has started.
9. **Add a Custom Field:**
   * Click the `+` next to the existing fields, choose `Single select`, name it `Priority`, and add options `High`, `Medium`, `Low`.
   * Set a priority value on each of your three issue cards.
10. **Close an Issue via Commit Message Automation:**
    * Open one of your three issues and note its number (e.g., `#4`).
    * Edit `README.md` and commit directly to `main` with the message `Fixes #4` (substituting the real issue number).
    * *Explanation:* Referencing an issue with a closing keyword in a commit message automatically closes that issue once the commit lands on the default branch.
11. **Verify the Automation:** Confirm the referenced issue is now closed, the milestone shows updated progress, and the project board reflects the issue's new state.
12. **Verify:** Confirm the `v1.0 Release` milestone shows accurate progress and the project board gives a clear, at-a-glance view of all three issues' current status and priority.

---
