## Lab 6: Sharing a Code Snippet Securely with Gists
**Real-World Scenario:** A colleague on Slack has asked you for a quick example of how you handle error retries in your service. It's not worth creating a full repository just to share ten lines of code.
**Why we are doing this:** Gists are the fastest way to share code outside a repository, but knowing the difference between public and secret is essential to avoid accidentally exposing something sensitive.

### Step-by-Step Instructions:
1. **Open Gist:** In your browser, go to `gist.github.com`.
2. **Add a Description:** In the description field, write a short summary, e.g., `Retry logic example`.
3. **Name Your File:** In the filename field, enter something like `retry.py` (or an extension matching a language you know).
4. **Write the Snippet:** In the content box, write a short 5–10 line example, such as a retry function.
5. **Publish as Public:**
   * Click the dropdown arrow next to `Create secret gist` and choose `Create public gist`.
   * *Explanation:* Public Gists are discoverable and embeddable — appropriate for a code example with nothing sensitive in it.
6. **Add a Second File:**
   * Click `Edit`, then `Add file`.
   * Give the new file a different name and a few lines of related content (e.g., a usage example calling the retry function).
   * Click `Update public gist`.
7. **Check Revision History:** Click the `Revisions` tab to see the change you just made recorded as a new version.
8. **Copy the Embed Code:** Click the `Embed` dropdown and copy the provided embed snippet (you don't need to use it, just confirm it's available).
9. **Create a Secret Gist for Comparison:**
   * Repeat steps 2–4 with a new snippet, but this time select `Create secret gist`.
   * *Explanation:* Secret means unlisted, not private — anyone with the exact URL can still view it, so never put real credentials or sensitive data in a Gist, public or secret.
10. **Verify Your Gist List:** Go to `gist.github.com/your-username` and confirm both Gists appear, and that you can distinguish which is public and which is secret.
11. **Share the Link:** Copy the public Gist's URL and confirm it opens correctly in a private/incognito browser window without requiring login.

---
