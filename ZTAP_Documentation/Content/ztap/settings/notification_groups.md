---
title: "Notification Groups"
weight: 1
---
![Notification Groups](/ztap/media/notification_groups_main.png)
Notification Groups allows you to create groups of users that you can specify to receive email and in-application notifications for different events such as new Alerts and Escalations. You can create multiple Notification Groups based on the needs of your Organization and configure schedules so that users who work at different times will only receive notifications during their working hours. 

You can also create individual Escalation Paths. An Escalation Path is a container with its own set of unique Notification Groups. You can use Escalation Paths to more easily route events to specific individuals or teams using [Playbooks](/ztap/orchestration/playbooks/).

### Create a new Notification Group
1. Go to **Settings** in the left side navigation, then click **Notification Groups** at the top.
2. Click **Create Group**.
![Create Notification Group](/ztap/media/notification_groups_create_1.png)
3. Type a name for the Notification Group and set the time for a user to respond before the next available Notification Group is notified. The default is 30 days.
4. Click **Save**.
5. To add users to your Notification Group, click **Add User** in the lower left.
6. Start typing the email address. The system will auto-fill as you type. Select the desired email address, then click Add User at the top.
7. After you have added a user, you can set the **Priority** for that user to **Default**, **Primary**, or **Secondary**. This is useful to inform other users of who to contact directly if additional information is required. The notifications sent to all users in the Notification Group are identical.
7. To set a schedule for when the Notification group is active, use the **Schedule settings on the left.
![Notification Group Schedule](/ztap/media/notification_groups_schedule.png)
8. Use the speech bubble icon to add any required comments to your Notification Group.

### Create a new Escalation Path
1. Click the **Escalation path** dropdown and select **New escalation path**.
![Create Escalation Path](/ztap/media/escalation_paths_create_1.png)
2. Type a name and description for your Escalation Path.
![Escalation Path Description](/ztap/media/escalation_paths_create_2.png)
3. Click **Create**.
4. Create individual Notification Groups in your Escalation Path to include the users and schedules where you want the Escalation Group to apply.

