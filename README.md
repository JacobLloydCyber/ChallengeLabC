<h1>Challenge Lab C: UNDER CONSTRUCTION!!!</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
The purpose of this lab....
<br />


<h2>Environments Used (POSSIBLY DELETE OR CHANGE) </h2>

- <b>Linux Ubuntu image in Virtualbox</b>

<h2>Key Points Within Lab: </h2>

- <b>Installation of Active Directory and creation of mydomain.com</b>
- <b>Routing enabled via configuration of RAS and NAT</b>
- <b>Configuration of DHCP for automatic IP addressing</b>
- <b>Powershell script for automatic user account creation</b>
- <b>Creation of user workstation (CLIENT1) and joining of CLIENT1 to mydomain.com</b>
- <b>Creation of various Security Groups for network division into specific departments</b>

<h2>Lab walk-through:</h2>

<p align="center">
Pictured below is a basic diagram of the full, configured network. The first VM, the domain controller (denoted DC) houses Active Directory and our domain (mydomain.com) via the installation of a Windows Server 2019 iso. This VM is configured to have two network adapters; one external adapter that connects to the internet, and one internal adapter that clients from inside the private network will connect to. The external NIC automatically receives IP addressing from my home router, while the internal NIC has IP addressing manually assigned to it. NAT and routing are configured on the domain controller allowing clients from the internal portion of the network a means to reach the internet through the domain controller. DHCP is configured with the info listed below so that our client machine (denoted CLIENT1, and using Windows 10) can automatically receive an IP address. CLIENT1 is joined to mydomain.com allowing any respective members to login and use this machine with their respective credentials. <br/>
<img src="https://i.imgur.com/BEFhvS2.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
Viewing the dashboard of AD server manager and all configured services on the domain controller:  <br/>
<img src="https://i.imgur.com/I5WX1Vs.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />

<p align="center">
DHCP enabled but still needs configuring: <br/>
<img src="https://i.imgur.com/E9V1kcS.png" height="80%" width="80%" alt="AD Home Lab"/>
<br />
<br />



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
