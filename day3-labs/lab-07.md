## Lab 7: Creating a Custom Secret Scanning Pattern
**Real-World Scenario:** Your fictional company issues its own internal API tokens in a specific format that no GitHub partner pattern would recognize, and you need to make sure secret scanning catches them too.
**Why we are doing this:** Custom patterns extend secret scanning's detection beyond partner-provided credentials to your organization's own internal token formats.

### Step-by-Step Instructions:
1. **Open Your Organization:** Navigate to your organization's `Settings`, then `Code security`.
2. **Open Custom Patterns:** Click `Secret scanning`, then find the section for custom patterns and click `New pattern`.
3. **Name the Pattern:** Enter a name such as `Internal API Token`.
4. **Define the Regular Expression:** In the pattern field, enter a regular expression matching a plausible internal token format, such as `internal_[a-z0-9]{32}`.
5. **Add a Test String:** In the testing area, paste a sample string matching your pattern, such as `internal_abcdefghijklmnopqrstuvwxyz012345`, and confirm it highlights as a match.
6. **Add a Non-Matching Test String:** Paste a string that should NOT match, such as `internal_short`, and confirm it is correctly not flagged.
7. **Set the Scope:** Choose whether this pattern applies to all repositories in the organization or a selected subset, and select an appropriate scope for testing.
8. **Save as a Dry Run First:** If available, save the pattern in a dry-run or test-only mode before fully publishing it.
9. **Review Dry-Run Results:** Check whether the dry run flags any unexpected matches across existing repository content, which would indicate the pattern is too broad.
10. **Publish the Pattern:** Once satisfied with the test results, publish the pattern for real.
11. **Test It Live:** In `org-service-lab`, create a file containing a string matching your custom pattern and attempt to commit it, confirming push protection (if also enabled) blocks it, or that a secret scanning alert is generated.
12. **Verify:** Confirm you can explain why testing a custom pattern against existing content before publishing broadly is an important step, not an optional one.

---
