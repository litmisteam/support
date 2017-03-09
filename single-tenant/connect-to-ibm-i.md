# Connect To IBM i

Included with each Litmis Space _Single_ Tenant base configuration is a browser-based customer-configurable firewall named [vCloud Director](http://pubs.vmware.com/vcd-80/index.jsp). By default the firewall is fairly locked down and you must log into it and configure your IP address to be allowed access to your IBM i. This documentation will walk you through that process. You should have received an email with the following information.

#### vCloud \(vShield Edge Gateway Firewall\) {#vcloud-vshield-edge-gateway-firewall}

**Firewall URL:**[https://cloud.domain.com/cloud/org/KT02-V999/](https://cloud.domain.com/cloud/org/KT02-V999/)  
**Username:**admin  
**Password:**xxxxxxxx

#### IBM i Instance {#ibm-i-instance}

**IBM i Internet IP:**66.186.999.999  
**IBM i Intranet IP:**192.168.0.2  
**Username:**QSECOFR  
**Password:**xxxxxxx

---

**Step 1:**Go to myglobalip.com and obtain your public IP so it can be put into the firewall.  
![](/assets/firewall_myglobalip.png "MyGlobalIP")

---

**Step 2:**Open the Firewall URL from your email and click on the below buttons and links.

![](/assets/firewall_vcloud1.png "vCloud 1")

**Step 3:**Select Edge Gateway tab, right click on the entry in the list and select Edge Gateway Services.  
![](/assets/firewall_vcloud2.png "vCloud 2")

**Step 4:**Add a Firewall entry for your public IP so you can connect to the IBM i public IP.  
![](/assets/firewall_vcloud3.png "vCloud 3")

After hitting OK above the firewall needs about 10 seconds to apply the new configuration and you are now ready to connect a 5250 telnet session using the _IBM i Public IP_ mentioned above \(the one from your email\).


