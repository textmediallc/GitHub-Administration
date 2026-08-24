## Lab 18: Reading Repository Health with Insights Graphs
**Real-World Scenario:** Your manager has asked you to give a two-minute status update on `team-service-lab` at tomorrow's standup, based only on what the repository's activity data shows in the UI.
**Why we are doing this:** GitHub's built-in Insights graphs let administrators and contributors assess a project's health at a glance, without manually reading through commit history.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab`, which should now have accumulated activity from several earlier labs.
2. **Open the Insights Tab:** Click `Insights` in the repository's top navigation.
3. **Review Pulse:**
   * With `Pulse` selected, note the date range shown and read the summary of merged pull requests, opened issues, and active contributors.
4. **Review the Contributors Graph:**
   * Click `Contributors` in the left sidebar.
   * Identify who has the most commits and roughly how additions and deletions are distributed.
5. **Review the Commits Graph:**
   * Click `Commits`.
   * Identify which week had the highest commit activity.
6. **Review Code Frequency:**
   * Click `Code frequency`.
   * Note whether additions or deletions dominate the recent history, and consider what that might indicate (new feature work versus cleanup).
7. **Review the Network Graph:**
   * Click `Network`.
   * Locate a point where a branch from an earlier lab diverged from `main` and where it merged back in.
8. **Check Traffic (Admin/Write Access Required):**
   * Click `Traffic`.
   * Note the views and clones data.
   * *Explanation:* Traffic is the one Insights graph restricted to users with write or admin access, since it reveals information about external interest the maintainers may not want fully public.
9. **Review Community Standards:** Click `Community` and note the checklist of recommended repository health files.
10. **Write Your Status Update:** In a new Gist (`gist.github.com`), write three sentences summarizing: (1) how many contributors have been active, (2) the general trend in commit activity, and (3) one observation from the Network graph about branching activity.
11. **Verify:** Share the Gist link with a classmate or your instructor and confirm your summary accurately reflects what the graphs show.

---
