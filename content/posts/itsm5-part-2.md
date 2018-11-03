---
title: "Configure ITSM 5.0 for ServiceNow Part 2"
date: 2018-11-03T11:32:16-05:00
draft: true
type: "post"
---
<h2>Installing Mid Server</h2>

Now that we have requested our instance, we can move onto creating a user for our mid server connection as well as configuring the mid server.
This is where you will need to make sure that you have the Windows machine ready that I mentioned in the previous post.
<p>
In the search bar in the upper left, type **User Administration**. Click **Users**.
<p>
<img src="/img/snow/install-midserver-01.png" width=800 />
<p>
Click **New**. Fill out the details for the new mid server user. Click **Submit**.
<p>
<img src="/img/snow/install-midserver-02.png" width=800 />
<p>
After submitting, you will be brought back to the user screen. Click your user to open their details.
<p>
<img src="/img/snow/install-midserver-03.png" width=800 />
<p>
At the bottom of the screen, Click **Edit** under **Roles**.
<p>
<img src="/img/snow/install-midserver-04.png" width=800 />
<p>
In the collection filter, type mid. Select mid and click the right facing arrow. Click **Save**.
<p>
<img src="/img/snow/install-midserver-05.png" width=800 />
<p>
You will see some confirmation messages. Click **Update**.
<p>
<img src="/img/snow/install-midserver-06.png" width=800 />
<p>
Type mid in the filter in the upper left. Click **Downloads**. Select the Windows 64 bit.
<p>
<img src="/img/snow/install-midserver-07.png" width=800 />
<p>
Download and extract this to the Windows server. Open the folder and Click **installer.bat**.
<p>
<img src="/img/snow/install-midserver-08.png" width=800 />
<p>
Enter the URL for your Service Now instance. You can get it from the instance status page.
<p>
Enter the login information for the user you just created. Click **Test your connection**. If successful, click **Next**.
<p>
<img src="/img/snow/install-midserver-09.png" width=600 />
<p>
In the MID server name box, type the name of your mid server. Click **Next**.
<p>
<img src="/img/snow/install-midserver-10.png" width=600 />
<p>
Validate everything looks right and click **Next**.
<p>
<img src="/img/snow/install-midserver-11.png" width=600 />
<p>
<p>
Click **Start MID Server**.
<p>
<img src="/img/snow/install-midserver-12.png" width=600 />
<p>
<p>
Back in the Service Now console, click **Servers**. Check the box next to your server and use the dropdown menu to select **Validate**.
<p>
<img src="/img/snow/install-midserver-13.png" width=800 />
<p>
<p>
Click **Save**.
<p>
<img src="/img/snow/install-midserver-14.png" width=800 />
<p>
<p>
Once the validation is complete, the state will be **Up** and the validated will be **Yes**.
<p>
<img src="/img/snow/install-midserver-15.png" width=800 />
<p>