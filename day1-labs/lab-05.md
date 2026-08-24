## Lab 5: Tuning Notifications for a Multi-Repository Workflow
**Real-World Scenario:** You've just joined a team that maintains several active repositories. By your second day, your inbox is flooded with GitHub notifications and you're starting to miss the ones that actually need your attention, like review requests.
**Why we are doing this:** Poorly tuned notifications either bury important activity in noise or cause people to miss it entirely. Configuring notifications deliberately is a habit every professional developer needs early on.

### Step-by-Step Instructions:
1. **Open Notification Settings:** Click your profile photo, select `Settings`, then click `Notifications` in the left sidebar.
2. **Set Your Default Notification Email:** Confirm the email address listed under `Default notification email` is the one you actually check regularly.
3. **Configure Participating Notifications:**
   * Find the `Participating` row.
   * Enable both `Web` and `Email` for this row.
   * *Explanation:* "Participating" covers anything where you're directly involved — assigned, mentioned, or requested as a reviewer — so this should always be reliable.
4. **Configure Watching Notifications:**
   * Find the `Watching` row and set it to `Web` only.
   * *Explanation:* Watching covers all activity in repositories you follow broadly; routing it to web-only keeps your email inbox from being overwhelmed.
5. **Review Automatic Watching:** Under `Automatically watch repositories`, decide whether new repositories you create or gain access to should be automatically watched, and set accordingly.
6. **Configure Actions Notifications:** Scroll to the `Actions` section and set it to notify you only for failed workflow runs on repositories you've been active in.
7. **Confirm Security Alerts Are On:** Locate the security alert notification setting and confirm it remains enabled, regardless of your other changes.
8. **Open Your Notifications Inbox:** Go to `github.com/notifications`.
9. **Practice Filtering:**
   * In the search bar, type `reason:mention` and press Enter to see only notifications where you were directly named.
   * Clear the filter and try `repo:owner/name` for a specific repository you belong to.
10. **Verify:** Confirm your Participating and Watching rows show the settings you configured, and that you can filter your inbox by reason and by repository.

---
