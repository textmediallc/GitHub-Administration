## Lab 7: Building a Team Wiki for Project Documentation
**Real-World Scenario:** Your team keeps onboarding notes and architecture decisions in scattered Slack messages and personal notes docs. New hires struggle to find anything, and the same questions get asked repeatedly.
**Why we are doing this:** A well-organized wiki gives a team a single, versioned home for documentation that doesn't belong in the README, and the entire thing can be built and maintained without ever leaving the browser.

### Step-by-Step Instructions:
1. **Open a Repository You Own:** Navigate to `readme-practice` (from Lab 4) or another repository you control.
2. **Enable the Wiki Feature:**
   * Click `Settings`, scroll to the `Features` section, and confirm the `Wikis` checkbox is enabled.
3. **Open the Wiki Tab:** Click `Wiki` in the repository's top navigation.
4. **Create the Home Page:**
   * Click `Create the first page`.
   * Keep the title as `Home`.
   * Write a short welcome paragraph describing the wiki's purpose.
5. **Build a Table of Contents:**
   * Add a `## Pages` heading.
   * Add a bulleted list with a placeholder link, e.g. `- [Setup Guide](Setup-Guide)`.
   * Click `Save Page`.
   * *Explanation:* Treating the Home page as a table of contents is the single highest-leverage habit for keeping a wiki navigable as it grows.
6. **Create a Second Page:**
   * Click `New Page` in the wiki sidebar.
   * Title it `Setup Guide`.
   * Add at least three sections with headings (e.g., `## Requirements`, `## Installation`, `## Troubleshooting`), each with a couple of bullet points.
   * Click `Save Page`.
7. **Link the Pages Together:** Return to the `Home` page and click your `Setup Guide` link to confirm it navigates correctly.
8. **Edit an Existing Page:**
   * Open `Setup Guide`, click `Edit`, and add one more bullet point under `Troubleshooting`.
   * Write a short edit summary in the box provided, and click `Save Page`.
9. **Review Page History:**
   * Click `Page History` in the wiki sidebar.
   * Confirm both the original version and your edit appear as separate entries.
   * Click `Compare` on the two most recent versions to see exactly what changed.
   * *Explanation:* Because a wiki is version-controlled like everything else on GitHub, every edit is tracked with the same kind of history and diff view you'd see on a regular file — entirely through the browser.
10. **Verify:** Confirm the `Home` page links correctly to `Setup Guide`, and that the page history shows a clear, readable record of your edits.

---
