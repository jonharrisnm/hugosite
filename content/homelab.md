---
title: "Home Lab"
date: 2018-10-30T13:12:54-05:00
draft: false
---

This is well I will lay out all of the info for my homelab.

Current Hardware:

Hosts:

3 x Dell PowerEdge R720s
    Each has:
        2 x Intel E5-2660 @ 2.2Ghz
        192GB ram
        1 x Samsung EVO 860 250GB (vSAN SSD Cache)
        5 x Samsung EVO 860 1TB (vSAN SSD Capacity)
        Dual 10GB ethernet

3 x SuperMicro Sys-E300-8Ds
    Each has:
        1 x Intel D-1518 @ 2.2Ghz
        64GB ram
        1 x Crucial MX300 275GB m.2 (vSAN SSD Cache)
        1 x Crucial MX300 1TB m.2 (vSAN Capacity)
        Dual 10GB ethernet

Network:

1 x UniFi Security Gateway 3P
1 x UniFi Switch 16XG
1 x UniFi Switch 48 POE-500W

Software:

vSphere 6.7U1
vCenter 6.7U1
NSX-V 6.4.3
Site Recovery Manager 8.1.0 (Using two clusters with two vCenters to mimic two sites)
vSphere Replication 8.1
vRealize Automation 7.5
vRealize Business 7.5
vRealize Operations 7.0
vRealize Log Insight 4.7
vRealize Lifecycle Manager 2.0
vRealize Network Insight 3.9
Horizon 7.6

OS:

Windows 2016
Ubuntu 18.04