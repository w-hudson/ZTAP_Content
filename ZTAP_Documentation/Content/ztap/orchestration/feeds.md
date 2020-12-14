---
title: "Feeds"
weight: 4
---
![Feeds](/ztap/media/feeds_main.png)
Feeds are an important component of the Orchestration features in ZTAP. A Feed is an element that can be used in a Filter or Playbook to replace the value in a key/value pair with a list of one or more static values. Feeds allow you to more easily create Filters and Playbooks based on longer lists of known information such as server names, expected users, in-house applications, expected connections (for example, RFC 1918), and other data. Using a Feed instead of individual values in a Filter or Playbook allows you to edit the values within the Feed without deactivating the associated Filters or Playbooks to edit the values.

### Creating a New Feed
![Create Feed](/ztap/media/feeds_create.png)
Perform the following steps to create a new Feed:
1. Select **Orchestration** from the left side navigation, then click **Feeds** at the top of the page.
2. Click **Create Feed** in the top right.
3. Give the Feed an identifiable name.
4. Select the **Organization** where you want to apply the Feed.
5. Choose a text file to upload or leave blank to create an empty Feed. If you select a file, the individual entries **must** be separated by a carriage return.

   **NOTE**: CIDR notation for IP addresses is supported.
6. Click **Create**.
  
### Editing a Feed
![Edit Feed](/ztap/media/feeds_edit.png)
Perform the following steps to edit an existing Feed:
1. Select the Feed you want to edit.
2. Click the **+** icon beside **Values** to add a value. Click the **-** icon beside an individual value to remove it.
3. Click **Save**. 
4. The Feed will now show as **Has Pending Changes**.
   ![Feed Pending Changes](/ztap/media/feeds_pending_changes.png)
5. The changes must be reviewed and approved by a Superuser for your organization before they will take effect in any Filters or Playbooks that use the Feed.

### Reviewing a Feed (Superuser only)
After a user creates or edits a Feed, it must be reviewed by a Superuser. To review a feed:
1. Select **Orchestration** from the left side navigation, then click **Feeds** at the top of the page.
2. Scroll or search to locate the Feed you need to approve and click the Feed name. You can also use the **Pending Changes** dropdown and select **Yes** to show only Feeds with pending changes. 
3. Click the name of the Feed you want to review.
4. Click the Changes tab in the reviewing pane and verify the data that has been changed.
   ![Review Feed](/ztap/media/feeds_review_1.png) 
5. Click **Apply** or **Reject** for each change, then click **Save**. If you rejected any of the changes, the user who requested the edit will be notified so that they can make any necessary corrections and re-submit the changes.

### Using Feeds in a Filter or Playbook
You can use Feeds in both Filters and Playbooks to replace the single value from an Alert with the list in the Feed. The example below shows how to use a Feed as a component of a Filter. For more detailed information, see [Filters](ztap/orchestration/filters/) or [Playbooks](ztap/orchestration/playbooks/).

1. Open the Alert that is the basis for your Filter or Playbook.
2. Click Create Filter or Create Playbook. For this example, we will create a Filter.
![Create Filter or Playbook](/ztap/media/create_filter_playbook.png)
3. Set the values for Organization, Product, and Tier.
4. Under Mandatory fields, click **Choose field** and select the Key where that applies to your Feed.
5. Click Match and select **In** or **Not In** depending on the logic you are using.
   - **In** specifies that the Filter applies only if the value is contained in the Feed.
   - **Not In** specifies that the Filter applies only if the value is **not** contained in the Feed. This functions similarly to a blacklist.
6. Start typing the name of your Feed in the value field, then select the name of the Feed you want to use.
![Feed Selection](/ztap/media/feed_use.png)
   
   **NOTE**: You can also use multiple values if you have not uploaded a Feed. Type each term you want to include, separated by commas (spaces after commas are accepted).
7. Add any other required fields and actions, then **Validate** and **Save** your Filter.
