## Lab 10: Configuring Large File Policies and Deploy Key Access
**Real-World Scenario:** A designer on your team wants to start committing large `.psd` design files into the project repository, and a build server needs read access to pull the repository automatically — without using anyone's personal account.
**Why we are doing this:** As an administrator, you set the policy for how large files are handled and control which non-human systems (servers, build pipelines) can access a repository — both of which are configured entirely through repository settings.

### Step-by-Step Instructions:
1. **Open Your Repository:** Navigate to `team-service-lab` from Lab 9.
2. **Create a Git Attributes File:**
   * Click `Add file`, then `Create new file`.
   * Name it `.gitattributes`.
   * Add the line: `*.psd filter=lfs diff=lfs merge=lfs -text`
   * *Explanation:* This line tells Git that any file matching `*.psd` must be handled by Git Large File Storage rather than stored directly in the repository's ordinary history — a policy you're setting centrally, before anyone commits a large file.
3. **Add a Second Large-File Pattern:** On a new line, add: `*.mp4 filter=lfs diff=lfs merge=lfs -text`
4. **Commit the File:** Write a commit message such as "Configure LFS policy for design and video assets", select `Commit directly to the main branch`, and click `Commit new file`.
5. **Review the Policy:** Open `.gitattributes` and confirm both lines are present exactly as written.
6. **Review Storage Usage:**
   * Click your profile photo, select `Settings`, then click `Billing and plans`.
   * Locate the section showing Git LFS data storage and bandwidth usage.
   * *Explanation:* GitHub enforces storage and bandwidth quotas for LFS on free plans — an administrator monitors this the same way they'd monitor any shared infrastructure cost.
7. **Open Deploy Key Settings:** Return to `team-service-lab`, click `Settings`, then click `Deploy keys` in the left sidebar.
8. **Add a Deploy Key:**
   * Click `Add deploy key`.
   * Give it a descriptive title, such as "Build Server".
   * Paste a sample SSH public key value provided by your instructor into the `Key` field.
9. **Set the Access Level:**
   * Leave `Allow write access` unchecked for a read-only key, appropriate for a server that only needs to pull code.
   * *Explanation:* A deploy key is a repository-scoped key, most often generated on a server rather than a person's laptop, and registering it here gives that server exactly the access it needs — no more — without tying access to any individual's account.
10. **Save the Deploy Key:** Click `Add key`.
11. **Verify:** Confirm the deploy key appears in the `Deploy keys` list with the correct title and access level, and that `.gitattributes` correctly lists both LFS-tracked file patterns.

---
