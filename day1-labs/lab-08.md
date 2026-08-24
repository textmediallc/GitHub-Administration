## Lab 8: Publishing a Project Site with GitHub Pages
**Real-World Scenario:** Your team has built a small internal tool and needs a simple landing page describing what it does and how to request access, without spinning up any real hosting infrastructure — and without waiting on a developer's local environment to be free.
**Why we are doing this:** GitHub Pages provides free, reliable static hosting directly from a repository — a practical option for documentation sites, portfolios, and small project pages, and the whole site can be built entirely through the browser.

### Step-by-Step Instructions:
1. **Create a New Repository:**
   * Click the `+` icon and select `New repository`.
   * Name it `pages-practice`, set it to `Public`, and check `Add a README file`.
   * Click `Create repository`.
2. **Create an HTML File:**
   * Click `Add file`, then `Create new file`.
   * Name the file `index.html`.
   * In the editor, write a simple page including `<html>`, `<head>` with a `<title>`, and a `<body>` with a heading and a short paragraph.
3. **Commit the File:** Scroll down, write a commit message such as "Add homepage", select `Commit directly to the main branch`, and click `Commit new file`.
4. **Enable GitHub Pages:**
   * Click the `Settings` tab, then click `Pages` in the left sidebar.
5. **Choose the Publishing Source:**
   * Under `Build and deployment > Source`, select `Deploy from a branch`.
   * Under `Branch`, select `main` and folder `/ (root)`, then click `Save`.
6. **Wait for the Build:** Wait one to two minutes, then refresh the Pages settings page until a green banner appears with your live site URL.
7. **View the Live Site:** Click the provided URL and confirm your HTML content renders correctly in a new tab.
8. **Make a Visible Update:**
   * Return to the repository, open `index.html`, and click the pencil icon.
   * Change the heading text and commit directly to `main`.
   * *Explanation:* Every commit to the publishing branch automatically triggers a new Pages deployment — no separate deploy step is needed.
9. **Verify the Update:** Wait about a minute, then refresh your live site and confirm the updated heading appears.
10. **Verify:** Confirm the live site loads at `your-username.github.io/pages-practice` and reflects your most recent edit.

---
