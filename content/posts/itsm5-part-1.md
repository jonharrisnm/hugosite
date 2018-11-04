---
title: "Configure ITSM 5.0 for vRA Part 1"
author: "Tom Burge"
date: 2018-11-03T11:32:14-05:00
draft: false
type: "post"
tags:
- vmware
- snow
- vra
- itsm
---

<h2>Requesting Service Now Instance</h2>

In this series, I will be configuring the brand new VMware vRealize Automation Plugin for ITSM 5.0 for ServiceNow London.

You can acquire the plugin from here: https://marketplace.vmware.com/vsx/solutions/vmware-vrealize-automation-plug-in-for-itsm-5-0-0

Download the XML plugin and the installation PDF.

Pre-requisites:<p>
<ul>
<li>vRealize Automation 7.5 configured with a tenant and necessary catalog items</li>
<li>Windows Server 2012R2 or 2016 with Java 1.8.0_152 or above</li>
</ul>

First step will be to get a developer instance of Service Now if you don't have one. If you do have one, you can skip to part 2.

Open a browser and navigate to https://developer.servicenow.com/app.do#!/home.
<p>
<img src="/img/snow/request-instance-01.png" width=800 />
<p>
Create an account if you don't have one. Log in if you do.
<p>
<img src="/img/snow/request-instance-02.png" width=800 />
<p>
Select **Manage** then **Instance**.
<p>
<img src="/img/snow/request-instance-03.png" width=800 />
<p>
Click **Request Instance**.
<p>
<img src="/img/snow/request-instance-04.png" width=800 />
<p>
Click **London**.
<p>
<img src="/img/snow/request-instance-05.png" width=800 />
<p>
After requesting the instance, you will be presented with the instance status screen. Take note of the URL then click the link to login.
<p>
<img src="/img/snow/request-instance-06.png" width=800 />
<p>
You will be prompted to reset your admin password and once you have, you will be at the home dashboard.
<p>
<img src="/img/snow/request-instance-07.png" width=800 />
<p>