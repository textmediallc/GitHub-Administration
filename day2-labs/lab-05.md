## Lab 5: Creating and Configuring a GitHub Organization
**Real-World Scenario:** Your company's engineering team has been using personal accounts for everything, and leadership has finally approved moving to a proper organization before the team grows further.
**Why we are doing this:** Every piece of team-based access control, security policy, and billing in the rest of this course depends on a correctly configured organization — this lab lays that foundation.

### Step-by-Step Instructions:
1. **Start Organization Creation:** Click the `+` icon in the top-right corner and select `New organization`.
2. **Choose a Plan:** Select the `Free` plan for this exercise.
3. **Name Your Organization:** Enter a unique organization name, such as `your-username-labs-org`, and enter a contact email.
4. **Confirm You're the Owner:** Confirm your account is listed as the organization's owner, then complete the verification step if prompted.
5. **Skip or Add Initial Members:** If prompted to invite teammates, you may skip this step for now — it will be practiced in the next lab.
6. **Open Organization Settings:** Once created, click `Settings` from your new organization's page.
7. **Review Organization Profile:** Under `Profile`, confirm the organization's display name and add a short description.
8. **Set the Default Repository Permission:**
   * Click `Member privileges` in the left sidebar.
   * Under `Base permissions`, confirm or set the level to `Read`.
   * *Explanation:* Setting this to Read means new members can see every repository by default but need an explicit team grant before they can push — the safer starting point discussed in Module 6.
9. **Review Repository Creation Policy:** Still under `Member privileges`, review who is allowed to create new repositories within the organization.
10. **Create a Repository Under the Organization:**
    * Click the `+` icon, select `New repository`, and choose your new organization as the owner.
    * Name it `org-service-lab`, set it `Public`, and check `Add a README file`.
    * Click `Create repository`.
11. **Verify:** Confirm `org-service-lab` appears under your organization's Repositories tab, and that the organization's base permission level is set to `Read`.

---
