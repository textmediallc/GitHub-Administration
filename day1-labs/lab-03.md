## Lab 3: Evaluating an Open-Source Repository Before Adoption
**Real-World Scenario:** Your team is considering pulling in a third-party open-source library for an upcoming project. Before anyone writes a single line of code against it, someone needs to confirm the library is actively maintained and safe to depend on.
**Why we are doing this:** Adopting an abandoned or poorly maintained dependency can create long-term technical debt and security risk. Knowing how to evaluate a repository's health is a core skill for any developer making dependency decisions.

### Step-by-Step Instructions:
1. **Open GitHub Explore:** In your browser, go to `github.com/explore`.
2. **Browse Trending Repositories:**
   * Filter by a language relevant to your team's stack.
   * Switch between `Daily`, `Weekly`, and `Monthly` to see how the list changes.
3. **Select a Candidate Repository:** Click into any repository that looks relevant to a real or hypothetical project need.
4. **Check Activity Signals:**
   * Note the star count and fork count near the top of the page.
   * Click the `Commits` link and check the date of the most recent commit.
   * *Explanation:* Recent commit activity is the single strongest signal that a project is still being maintained.
5. **Check the Issue Tracker:**
   * Click the `Issues` tab.
   * Look at how many issues are open versus closed, and whether recent issues have maintainer responses.
6. **Check for a License:**
   * Look for a `LICENSE` file in the file list, or check the `About` panel on the right side of the repo homepage.
   * *Explanation:* Without a license, technically no one else has clear legal permission to use the code, even if the repository is public.
7. **Check the README Quality:**
   * Confirm the README includes installation instructions and usage examples.
8. **Open the Insights Tab:**
   * Click `Insights`, then `Pulse`, to see a summary of recent merged pull requests, opened issues, and active contributors.
9. **Document Your Findings:** In a new Gist (`gist.github.com`), write two or three sentences evaluating whether this repository appears well-maintained, citing the specific signals you checked.
10. **Repeat for a Second Repository:** Use the search bar with a query like `topic-name language:javascript stars:>1000` to find a second candidate, and repeat steps 4–8 to compare.

---
