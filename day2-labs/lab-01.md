## Lab 1: Mastering GitHub Search Syntax and Saved Searches
**Real-World Scenario:** A configuration key is being renamed across your company's codebase, and you've been asked to find every file across every repository in your organization that still references the old name — before anyone spends a day doing it by hand.
**Why we are doing this:** GitHub's search syntax is one of the highest-leverage tools an administrator has for answering "where else does this exist?" questions across dozens of repositories at once, entirely from the browser.

### Step-by-Step Instructions:
1. **Open GitHub Search:** On `github.com`, click the search bar at the top of any page.
2. **Run a Basic Query:** Type `readme` and press Enter, then review the default results.
3. **Switch Search Types:** Click through the `Code`, `Issues`, `Repositories`, and `Commits` tabs above the results and note how the results change for each.
4. **Scope a Search to Your Own Work:** Clear the search box and enter `user:your-username` (replacing with your actual username), then press Enter.
5. **Scope a Search to a Repository:** Enter `repo:your-username/team-service-lab` to narrow results to a single repository from an earlier lab.
6. **Search for a Specific String in Code:**
   * Click the `Code` tab.
   * Enter `NOTES.md in:path` to find repositories where that file path exists.
7. **Filter by Language:** Modify the query to add `language:markdown` and note how results narrow further.
8. **Search Issues by State:**
   * Click the `Issues` tab.
   * Enter `is:issue is:open` and review any open issues across repositories you have access to.
9. **Combine Multiple Qualifiers:** Enter `is:pr is:merged` to see merged pull requests, then add `author:your-username` to narrow to your own.
10. **Filter by Date:** Add `merged:>2020-01-01` to the query and confirm the date qualifier narrows results as expected.
11. **Bookmark a Useful Query:**
    * Once you've built a query you'd realistically reuse (such as `is:pr is:open review-requested:your-username`), copy the full URL from your browser's address bar.
    * Save it as a browser bookmark labeled "My Pending Reviews."
    * *Explanation:* GitHub doesn't have a dedicated "saved search" feature, so a bookmarked query URL is the standard way administrators keep frequently used searches within one click.
12. **Verify:** Confirm you can explain, in one sentence each, what `org:`, `is:`, `language:`, and a date comparison qualifier each do.

---
