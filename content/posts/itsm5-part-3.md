---
title: "Configure ITSM 5.0 for ServiceNow Part 3"
author: "Tom Burge"
date: 2018-11-03T11:32:18-05:00
draft: false
type: "post"
tags:
- vmware
- snow
- vra
- itsm
---
<h2>Installing and Configuring Plugin</h2>

Now that we have finished requesting our instance and creating our MID server, we will move onto install and configuring the plugin.

<p>
Here we are starting at the home dashboard.
<p>
<img src="/img/snow/install-plugin-01.png" width=800 />
<p>
In the upper left filter, type update sets and click **Update Sources**.
<p>
<img src="/img/snow/install-plugin-02.png" width=800 />
<p>
Click **Choose File** and browse to the XML file you downloaded from the marketplace. Click **Upload**.
<p>
<img src="/img/snow/install-plugin-03.png" width=800 />
<p>
After the upload completes, you will be redirected to the Update Sets list. Click **VMware vRealize Automation Application**.
<p>
<img src="/img/snow/install-plugin-04.png" width=800 />
<p>
Click **Preview Update Set**.
<p>
<img src="/img/snow/install-plugin-05.png" width=800 />
<p>
The Update Set Preview will give an error and this is normal. Click **Close**.
<p>
<img src="/img/snow/install-plugin-06.png" width=800 />
<p>
Scroll to the bottom of the page and select the check boxes next to the four items. Use the dropdown to select **Accept remote update**.
<p>
<img src="/img/snow/install-plugin-07.png" width=800 />
<p>
You will receive some messages saying that the problems have been addressed. Click **Commit Update Set**. This is going to take awhile.
<p>
<img src="/img/snow/install-plugin-08.png" width=800 />
<p>
Click **Update Sources**. You can see that the vRA application is there.
<p>
<img src="/img/snow/install-plugin-09.png" width=800 />
<p>
Click **Update log**. There are 3011 items that need to complete. When it is done, you will see **Finished update load from database**.
<p>
<img src="/img/snow/install-plugin-10.png" width=800 />
<p>
In the upper left filter, type script include. Click **Script Includes**. Search for **JSUtil** and click on the name to open it.
<p>
<img src="/img/snow/install-plugin-11.png" width=800 />
<p>
In the upper right, use the dropdown labeled **Accessible from** and select **All application scopes**. Click **Update**.
<p>
<img src="/img/snow/install-plugin-12.png" width=800 />
<p>
In the upper left filter, type **tables**. Under **System Definition**, click **Tables**. In the search, type **user_criteria**.
<p>
<img src="/img/snow/install-plugin-13.png" width=800 />
<p>
Click **User Criteria** to open the item.
<p>
<img src="/img/snow/install-plugin-14.png" width=800 />
<p>
Make sure all of the following boxes are checked:
<ul>
    <li>Can read</li>
    <li>Can create</li>
    <li>Can update</li>
    <li>Can delete</li>
</ul>
Click **Update**. 
<p>
<img src="/img/snow/install-plugin-15.png" width=800 />
<p>
Repeat for all of the below tables:
<ul>
    <li>user_criteria</li>
    <li>sc_category_user_criteria_mtom</li>
    <li>item_option_new</li>
    <li>catalog_script_client</li>
    <li>question_choice</li>
    <li>catalog_ui_policy</li>
    <li>catalog_ui_policy_action</li>
    <li>sc_cat_item_user_criteria_mtom</li>
    <li>sc_req_item</li>
    <li>sc_category</li>
</ul>
<p>
In the upper left filter, type users.
Here we are going to configure the users that can access vRealize Automation. I am going to use the admin account, but you can use any account.
Search for System Administrator and click the user ID.
Click **Edit** under **Roles**.
<p>
<img src="/img/snow/install-plugin-16.png" width=800 />
<p>
Search for and add the following roles:
<ul>
<li>itil</li>
<li>x_vmw_vmware_vrasp.vra_user --- **Any user that uses vRA will need this role.**</li> 
<li>x_vmw_vmware_vrasp.vrealize_automation_catalog_admin</li>
</ul>
Click **Save**.
<p>
<img src="/img/snow/install-plugin-17.png" width=800 />
<p>
Click **Groups**.
<p>
<img src="/img/snow/install-plugin-18.png" width=800 />
<p>
 Click **Edit**.
<p>
<img src="/img/snow/install-plugin-19.png" width=800 />
<p>
Search for **vRealizeAutomation-ApprovalManagersGroup** and add it to the list. Click **Save**.
<p>
<img src="/img/snow/install-plugin-20.png" width=800 />
<p>
Click **Update**.
<p>
<img src="/img/snow/install-plugin-21.png" width=800 />
<p>
Before we register vRA into Service Now, we need to create a service account in vRA and add it to all of the business groups as a **Business Group Manager**. Once this is complete, you can continue.
<p>
<img src="/img/snow/install-plugin-23.png" width=800 />
<p>
In the upper left filter, type vRealize. Click **Register vRAs**.
<p>
<img src="/img/snow/install-plugin-24.png" width=800 />
<p>
<ul>
<li>Name: </li>
<li>HostName: https://[urlofvRA]</li>
<li>Tenant Name: [Only one tenant is supported per vRA]</li>
<li>MidServer: [Select the MID server we created earlier.]</li>
<li>Service User UserName: [Enter the service account in vRA that you created.]</li>
<li>Service User Password: [Enter the password for that account.]</li>
</ul>
Click **Save**.
<p>
<img src="/img/snow/install-plugin-25.png" width=800 />
<p>
Your instance of vRA is now registered. We have to perform imports of the catalog and CMDB. Click the name of vRA to open it.
<p>
<img src="/img/snow/install-plugin-26.png" width=800 />
<p>
Click **Import Services and Catalog Items**.
<p>
<img src="/img/snow/install-plugin-27.png" width=800 />
<p>
Click **Scheduled Imports Queue**. This may take a bit depending on your vRA.
<p>
<img src="/img/snow/install-plugin-28.png" width=800 />
<p>
Refresh until the queue is empty.
<p>
<img src="/img/snow/install-plugin-29.png" width=800 />
<p>
Go back into your registered vRA instance and click **Import and Reconcile CMDB**.
<p>
<img src="/img/snow/install-plugin-30.png" width=800 />
<p>
Click **Scheduled Imports Queue**.
<p>
<img src="/img/snow/install-plugin-31.png" width=800 />
<p>
Refresh until empty. Click **vRealize Automation User Portal** when clear.
<p>
<img src="/img/snow/install-plugin-32.png" width=800 />
<p>
Here is the brand new portal for the vRA integration. Prior to this, we could only see catalog items, but now you can see deployments and machines as well as perform day 2 actions. Congrats!
<p>
<img src="/img/snow/install-plugin-33.png" width=800 />
<p>
