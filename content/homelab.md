---
title: "Home Lab"
date: 2018-10-30T13:12:54-05:00
draft: false
---

This is where I will lay out all of the info for my homelab.<p>

Current Hardware:<p>

Hosts:<p>

3 x Dell PowerEdge R720s<p>
    Each has:<p>
        <ul>
        <li>2 x Intel E5-2660 @ 2.2Ghz
        <li>192GB ram
        <li>1 x Samsung EVO 860 250GB (vSAN SSD Cache)
        <li>5 x Samsung EVO 860 1TB (vSAN SSD Capacity)
        <li>Dual 10GB ethernet
        </ul>

3 x SuperMicro Sys-E300-8Ds<p>
    Each has:<p>
        <ul>
        <li>1 x Intel D-1518 @ 2.2Ghz
        <li>64GB ram
        <li>1 x Crucial MX300 275GB m.2 (vSAN SSD Cache)
        <li>1 x Crucial MX300 1TB m.2 (vSAN Capacity)
        <li>Dual 10GB ethernet
        </ul>

Network:<p>

<ul>
<li>1 x UniFi Security Gateway 3P
<li>1 x UniFi Switch 16XG
<li>1 x UniFi Switch 48 POE-500W
</ul>

Software:<p>

<ul>
<li>vSphere 6.7U1
<li>vCenter 6.7U1
<li>NSX-V 6.4.3
<li>Site Recovery Manager 8.1.0 (Using two clusters with two vCenters to mimic two sites)
<li>vSphere Replication 8.1
<li>vRealize Automation 7.5
<li>vRealize Business 7.5
<li>vRealize Operations 7.0
<li>vRealize Log Insight 4.7
<li>vRealize Lifecycle Manager 2.0
<li>vRealize Network Insight 3.9
<li>Horizon 7.6
</ul>

OS:<p>

<ul>
<li>Windows 2016
<li>Ubuntu 18.04
</ul>