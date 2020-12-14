---
title: "Lists"
weight: 3
---
![Lists](/ztap/media/lists_main.png)
Lists, often referred to as either the Whitelist or Blacklist, are a key feature of orchestration within ZTAP. Lists evaluate items by their individual hash values, rather than key/value pairs. Lists function similarly to [Filters](/ztap/orchestration/filters/), but the two fulfill different purposes - Lists identify very specific files or processes, while Filters use other data for more nuanced behavioral detection. Individual hash values must be explicity added to Lists by a user.

Like [Filters](/ztap/orchestration/filters/), Lists evaluate and categorize the events they match within ZTAP. Lists act as either a Tier 3 Filter (Whitelist) or Tier 1 Filter (Blacklist) that will recategorize any future events with the same hash value. Whitelisted events that are potentially related to an Alert will still be shown in the **Whitelisted Events** tab. See [Event Tiers](/ztap/hud/event_tiers/) for additional information on each Tier.

A defining feature of Lists is that they have the ability to utilize the APIs of the associated security products to send a hash value to the product’s console. For example, when you create a new whitelist entry for the target file hash of a Cylance **threat_quarantined** event, afer the List entry is reviewed and activated, it will evaluate and categorize the Cylance event within ZTAP and send the hash to the Global Whitelists within the Cylance console so that Cylance will also recognize the whitelisted hash. This is only available for products with an API that supports this functionality.  

New List entries are added to the Whitelist by default. After you create a new List item, you can modify the entry to instead add it to the Blacklist within ZTAP. For products that do not have a Blacklist API, this will behave similarly to a Tier 1 Filter, in that it will bypass any other Filter logic and create an Alert when an event with that hash is observed.
 
### Creating a new List entry
1. Open the Alert in ZTAP and navigate to the specific event.
2. Ensure that the event includes a hash value (SHA256 or MD5).
3. Click **Whitelist** on the left, then click **Yes** when you are prompted to confirm.
![Create List Entry](/ztap/media/lists_create_1.png)
4. To view and modify the new List entry, select **Orchestration** from the left side navigation, then click **Lists** at the top of the page.
5. Click the name of the entry you created and ensure that the information is correct.
   - To change the new entry to the Blacklist, click the entry and use the **Type** dropdown to select **Blacklist**.
![List Details](/ztap/media/lists_details.png)
6. Add any relevant comments to explain why the Lists entry was created.
7. Click the **Test List** tab to see a list of current Alerts that will be affected by the new entry.
8. Click **Save**.

### Reviewing and activating Lists
After a user creates a new List entry, it must be reviewed and activated by a Superuser.
1. Select **Orchestration** from the left side navigation, then click **Lists** at the top of the page.
2. Click the Lists entry that requires review.
3. Review the entry, supporting comments, and validate other affected Alerts under the **Test List** tab.
![Review List Entry](/ztap/media/lists_details.png)
5. Add any additional comments, then click **Activate** to approve the new List entry for use.
 
### Best Practices 
Because Lists are specific to hash values, they will only apply to a file that exactly matches a hash that is already captured in Lists. Similar Alerts with any difference in hash value will not be recognized.

CRITICAL**START** recommends that you use [Filters](/ztap/orchestration/filters/) for behavioral detections, as the key/value pairs in the data from your security products provide more control over the types of behavior that correspond to an event type.
