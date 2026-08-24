## Lab 17: Importing a Repository into GitHub Using the Web Importer
**Real-World Scenario:** A team is migrating a project from another Git hosting provider into your organization's GitHub account, and you've been asked to bring it over without disrupting its commit history.
**Why we are doing this:** GitHub Importer lets an administrator migrate a project from another host or version control system entirely through the browser — a task that comes up whenever a team consolidates onto GitHub.

### Step-by-Step Instructions:
1. **Open the Importer:** In your browser, go to `github.com/new/import`.
2. **Enter the Source URL:** In the `Your old repository's clone URL` field, enter `https://github.com/octocat/Spoon-Knife.git` as a stand-in for an external source repository.
   * *Explanation:* In a real migration this URL would point to a repository on another host (GitLab, Bitbucket, an internal Git server); using a public GitHub repository here lets you safely practice the exact same workflow.
3. **Continue to the Next Step:** Click `Begin import`.
4. **Choose the Destination Owner:** Confirm your personal account (or a practice organization, if you belong to one) is selected as the owner for the new repository.
5. **Name the New Repository:** Enter `imported-project-lab` as the repository name.
6. **Set Visibility:** Choose `Public` for this exercise.
7. **Start the Import:** Click `Begin import` and wait for GitHub to report that the import completed successfully.
8. **Review the Imported Repository:** Once finished, click the link to open `imported-project-lab`.
9. **Verify Commit History Was Preserved:**
   * Click `Commits` near the top of the file list.
   * Confirm the commit history matches the original source repository, including original author names and timestamps, rather than showing a single fresh commit.
   * *Explanation:* Preserving original commit history and authorship is the main advantage of using the Importer over manually recreating a project from scratch.
10. **Review the Repository's Branches:** Click the branch dropdown and confirm any branches from the source repository were carried over.
11. **Verify:** Compare `imported-project-lab` side-by-side with `octocat/Spoon-Knife` in two browser tabs and confirm the file contents match.

---
