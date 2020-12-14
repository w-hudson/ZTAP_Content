---
title: "Filters"
weight: 1
---
![Filters](/ztap/media/filters_main.png)
Filters automatically categorize and resolve security events that you have previously investigated. This allows security analysts to focus on new activity in ZTAP without turning off functionality in your installed security products.

Filters use key/value pairs from security events to identify known good behavior and automatically resolve future security events that match the logic created in the Filter.

### Create a new Filter

1.	Open the Alert and click **Create Filter**.
![Create Filter](/ztap/media/create_filter_playbook.png)
2.	Type a **Title** for the filter.
3.	Ensure that the **Organization**, and **Event Tier** are correct.
![Create Filter](/ztap/media/filters_create_1.png)
    - The Organization field defaults to the Organization where the source event originated. For an Organization with multiple child Organizations, you can select a specific child Organization or the top-level parent Organization to apply it to all child Organizations.
    - The default event Tier for Filters is **Tier 2** (Observations). This event type will not generate an Alert, but may be useful for additional investigative context for other Alerts. You can also select **Tier 3** (Safe) to whitelist an event or **Tier 4** (Discard) to have the platform discard activity that matches your filter. For additional information on the event Tiers and their uses, see [Event Tiers](/ztap/alerts/event_tiers/).
   
4.	Configure the details you want to use for the Filter logic:
![Mandatory and Optional Fields](/ztap/media/filters_create_3.png)
    - For the **Mandatory Fields**, select key/value pairs from the details of the Alert that match the criteria you want to filter. 
    You can add multiple fields to ensure that only known good events match the filter; the more specific your criteria, the less likely you are to miscategorize an event. All Mandatory Fields must match the event for the filter to apply.
    - **Optional Fields** can be useful to tune the logic of your Filter or add qualifying values. Multiple Optional Fields act with a Match Any operator - if any individual Optional Field matches, then the Filter is applied. 
    - If the Key/Value pairs in the security event do not provide enough context to safely filter the event, you can use **Advanced Filters** to collect additional validation data from your available Threat Analytics Plugins (TAPs). This turns the filter into a **Multi-Stage Filter** (MSF). 
![Advanced Filters](/ztap/media/filters_advanced_1.png)
    The Advanced Filter stage of an MSF uses Mandatory and Optional fields for the key/value pairs returned by the TAP. Because some TAPs return multiple pages of data, Advanced Filters can use the **Match Any** or **Match All** operators for the returned TAP data.    
![Advanced Filter Logic](/ztap/media/filters_advanced_3.png)
    After you have built the MSF logic, click  **Preview TAP** in the top right. If the Advanced Filter logic matches, a green checkmark will appear. If it fails, a red x will appear. When you receive a successful result, click **Add TAP** to add the TAP to your base filter. 
    
5.	Add Comments to describe the reason you created the Filter and any additional information.
6.	Click **Validate** to see a list of all current Alerts that would be affected by your new Filter and modify the logic as necessary so that only the corresponding Alerts are filtered.
7.	When you are satisfied that the filter will only affect expected events, click **Save**. The Filter must be reviewed by a Superuser before it becomes active.

### Editing a Filter
If you need to modify a Filter, you can edit its settings under Orchestration.
1. Go to **Orchestration**, **Filters**.
2. Open the Filter and make any necessary changes.
3. Add Comments to note any changes.
4. Click **Validate** at the bottom of the screen to test your changes.
5. Click **Save** at the bottom of the screen. 

### Reviewing and Activating a Filter
Before a new or modified Filter can become active, it must be reviewed by a Superuser.
1. Select **Orchestration** from the left side navigation, then click **Filters** at the top of the page.
2. Scroll, search, or use the drop-downs to locate the Filter.
3. Click **Assign to me** to start the review.
4. Check the details and Filter logic, then click **Validate** to ensure that only the expected events are affected by the filter.
5. Add Comments to note any changes to the Filter.
6. When you are satisfied that the Filter is configured correctly, click **Activate**.
