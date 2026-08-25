## Lab 2: Creating and Testing a Webhook
**Real-World Scenario:** Your team wants a Slack-style notification the moment someone opens a new issue on a key repository, and you've been asked to prototype the webhook before connecting it to a real chat integration.
**Why we are doing this:** Understanding how to configure, deliver, and verify a webhook — entirely through the Settings UI — is foundational to connecting GitHub to any external system.

### Step-by-Step Instructions:
1. **Get a Test Endpoint:** In a new browser tab, go to a webhook-testing site such as `webhook.site` and copy the unique URL it generates for you.
2. **Open Your Repository:** Navigate to `team-service-lab` on `github.com`.
3. **Open Webhook Settings:** Click `Settings`, then `Webhooks` in the left sidebar.
4. **Add a Webhook:** Click `Add webhook`.
5. **Enter the Payload URL:** Paste the test URL you copied in Step 1 into the `Payload URL` field.
6. **Set the Content Type:** Change `Content type` to `application/json`.
7. **Add a Secret:** In the `Secret` field, enter a sample passphrase, such as `lab-secret-value`.
   * *Explanation:* The secret lets a receiving system verify that a payload genuinely came from GitHub, by recomputing a signature and comparing it to the one GitHub sends.
8. **Choose Events:**
   * Select `Let me select individual events`.
   * Check `Issues` and uncheck everything else.
9. **Create the Webhook:** Confirm `Active` is checked, then click `Add webhook`.
10. **Trigger the Webhook:**
    * Click `Issues`, then `New issue`.
    * Give it a title and click `Submit new issue`.
11. **Verify the Delivery Arrived:** Return to your webhook-testing site tab and confirm a new POST request appears with a JSON payload describing the issue you just created.
12. **Review Delivery History in GitHub:**
    * Back in `Settings > Webhooks`, click on your webhook.
    * Click the `Recent Deliveries` tab and open the delivery that was just sent.
    * Review the request headers, the payload body, and the response returned by your test endpoint.
13. **Practice a Redelivery:** Click `Redeliver` on that same delivery and confirm a second matching request arrives at your test endpoint.
14. **Verify:** Confirm you can locate a webhook's full delivery history, including headers and payload, entirely from the Settings UI.

---
