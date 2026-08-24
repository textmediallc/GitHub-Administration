## Lab 19: Customizing a GitHub Pages Site Using the Web Editor
**Real-World Scenario:** The basic Pages site your team published in an earlier lab works, but it looks unstyled, and marketing has asked what it would take to eventually point a real company domain at it — and they'd like you to make the change without waiting on a developer's local setup.
**Why we are doing this:** Knowing how to apply a theme and prepare for a custom domain entirely through the browser lets an administrator take a Pages site from "functional" to "presentable" without needing a local development environment.

### Step-by-Step Instructions:
1. **Open Your Pages Repository:** Navigate to `pages-practice` from an earlier lab.
2. **Create a Jekyll Configuration File:**
   * Click `Add file`, then `Create new file`.
   * Name the file `_config.yml`.
   * In the editor, add the line: `theme: jekyll-theme-minimal`
   * *Explanation:* GitHub Pages has built-in support for a set of Jekyll themes — setting this one line applies professional styling without writing any CSS.
3. **Commit the File:** Scroll down, write a commit message, select `Commit directly to the main branch`, and click `Commit new file`.
4. **Wait for the Rebuild:** Allow about a minute for GitHub Pages to rebuild the site.
5. **Verify the Theme Applied:** Open `Settings > Pages`, click the live site URL, and confirm the site's appearance has changed.
6. **Explore Custom Domain Settings:**
   * Return to `Settings > Pages`.
   * Under `Custom domain`, note the input field where a real domain (e.g., `www.example.com`) would be entered.
7. **Add a Placeholder CNAME File:**
   * Click `Add file`, then `Create new file`.
   * Name it exactly `CNAME` (no extension).
   * Add a single line with a placeholder domain, such as `example.com`.
   * *Explanation:* In a real deployment, this file — combined with DNS records configured with your domain registrar — is what tells GitHub which custom domain should route to this Pages site.
8. **Commit the CNAME File:** Commit directly to `main` with a clear message.
9. **Review the Enforce HTTPS Option:** Return to `Settings > Pages` and locate the `Enforce HTTPS` checkbox, noting that it only becomes available once a real domain's certificate has been provisioned.
10. **Clean Up:** Since `example.com` is not a domain you control, remove the placeholder file to avoid leaving your Pages site in a broken state:
    * Open `CNAME`, click the trash can icon, write a commit message, and commit directly to `main`.
11. **Verify:** Confirm your live Pages URL still loads correctly at `your-username.github.io/pages-practice` after removing the CNAME file.

---
