## Lab 3: Building Your First GitHub Actions Workflow
**Real-World Scenario:** Your team has no automated checks at all — every typo and broken link in project documentation is currently caught by hand, if it's caught at all. You've been asked to add a simple automated check.
**Why we are doing this:** Writing and running a first GitHub Actions workflow, entirely through the web editor, is the foundation for every CI/CD task an administrator will configure going forward.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab`.
2. **Create the Workflows Folder:**
   * Click `Add file`, then `Create new file`.
   * In the filename field, type `.github/workflows/hello-actions.yml` (typing each `/` creates the folder automatically).
3. **Write the Workflow:** In the editor, enter the following YAML:
   ```
   name: Hello Actions

   on:
     push:
       branches: [main]
     workflow_dispatch:

   jobs:
     say-hello:
       runs-on: ubuntu-latest
       steps:
         - name: Checkout repository
           uses: actions/checkout@v4
         - name: Print a greeting
           run: echo "Hello from GitHub Actions, triggered on the ${{ github.ref_name }} branch"
   ```
4. **Commit the Workflow File:** Scroll down, write a commit message such as "Add first Actions workflow", select `Commit directly to the main branch`, and click `Commit new file`.
5. **Watch It Run Automatically:**
   * Click the `Actions` tab at the top of the repository.
   * Confirm a new run named "Hello Actions" appears, triggered by your commit.
6. **Review the Run:**
   * Click into the run, then click the `say-hello` job.
   * Expand the `Print a greeting` step and confirm your message appears in the log output.
7. **Trigger It Manually:**
   * Return to the `Actions` tab and click `Hello Actions` in the left sidebar.
   * Click `Run workflow`, confirm `main` is selected, and click the green `Run workflow` button.
   * *Explanation:* This works because the workflow includes `workflow_dispatch` as a trigger, which adds this manual "Run workflow" button.
8. **Confirm the Manual Run:** Refresh the run list and confirm a second run appears, this time triggered manually rather than by a push.
9. **Review Run History:** Confirm both runs are listed with their trigger type, duration, and status (green checkmark for success) visible directly in the Actions tab.
10. **Verify:** Confirm you can explain what each top-level YAML key (`name`, `on`, `jobs`, `steps`) in your workflow file does.

---
