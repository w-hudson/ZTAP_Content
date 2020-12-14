---
title: "Organizations"
weight: 6
---
The **Organizations** screens are where you manage the information for any Organizations you have permissions to access and the [Users](#users-&-roles) in your Organizations. 

### Organizations
![Organizations](/ztap/media/organizations_main.png)
This screen allow you to manage the settings for your primary Organization and any child Organizations you have created. Your primary Organization is configured by CRITICAL**START** when your service becomes active.

#### Edit Organization Details
To update the information for your Organization:
1. Click the name of the Organization you want to modify.
![Organizations](/ztap/media/organizations_manage_1.png)
2. Update the details for your Organization.

   **NOTE**: If you select **Require Multi-Factor Authentication** (MFA), users must provide a token from your configured MFA provider when they log in to ZTAP. Users will be prompted with the QR code on their initial login.
3. Click **Save**.

#### Create a New Organization
You can create additional child Organizations for specific departments or physical locations. You can then assign users to specific child Organizations. 
1. Click **Add Organization**.
2. Input the details for your Organization.

   **NOTE**: If you select **Require Multi-Factor Authentication** (MFA), users must provide a token from your configured MFA provider when they log in to ZTAP. Users will be prompted with the QR code on their initial login.
3. Use the drop-down menu to select the parent Organization.
4. Ensure all of the details are correct, then click **Save**.

### Users & Roles
![Users & Roles](/ztap/media/users_main.png)
Users and Roles allows you to manage the users in your organization who have access to ZTAP.

#### Add a new user
To add a new user to ZTAP:
1. Click **Organizations** in the left side navigation, then click **Users & Roles**.
2. Click **Invite User** on the right.
![Invite User](/ztap/media/users_invite_1.png)
3. Type the new user's email address and use the dropdown menu to select the Role you want to assign to the user. The basic Roles in ZTAP are:
   - **Read-only**: User has access to log in and view data, but is unable to make changes.
   - **User**: User can log in and interact with the platform, but changes such as creating Filters, Playbooks, Lists, and Feeds must be approved by a Superuser.
   - **Superuser**: User can create and approve changes to Filters, Playbooks, Lists, and Feeds. User can manage other user accounts and most settings for your Organization. Superuser accounts have administrative access for your Organization.
   
4. Click **Send Invitation**. 
5. The new user will receive an email with instructions to create a password and log in for the first time.

#### Manage users
You can manage the settings for any user account including User Name, Email address, Phone number, and active status. Scroll or search to locate the user account you want to modify and click the name of the user. 
![Manage User](/ztap/media/users_manage_1.png)

You can also change a users's password or request Single Sign On access for a user here.
![Change Password](/ztap/media/users_password_1.png)
