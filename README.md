# Creating Resources - Target VMs

<h2>Purpose</h2>

- Set up a Windows and Linux virtual machine.
- Configure inbound rule on their respective network security groups (NSGs) to allow all traffic from the Internet.
- Disable Windows Firewall from within windows-vm.

#
<h3>Create the Honeypot VMs - Windows and Linux</h3>
<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Creating-Resources-Target-VMS-Images/main/1.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Creating-Resources-Target-VMS-Images/main/2.png"/>

Create 2 VMs:
- windows-vm
- linux-vm

Make sure they share the following configurations:
- Subscription
- Region
- Resource group: RG-Cyber-Lab
- Virtual Network: Lab-VNet

#
<h3>Change NSG Inbound Rule: Allow All Traffic</h3>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Creating-Resources-Target-VMS-Images/main/3.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Creating-Resources-Target-VMS-Images/main/4.png"/>

Navigate to the network settings of windows-vm, scroll down to the Network Security Group configurations.

Delete the default inbound port rule.

Create a new port rule allowing all inbound traffic. This will allow all traffic from the Internet to the VM. 

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Creating-Resources-Target-VMS-Images/main/5.png"/>

Repeat the same steps for linux-vm.

#
<h3>Disable Windows Firewall</h3>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Installing-Microsoft-SQL-Server-Images/main/1.png"/>

Ping the windows-vm from your host machine using windows-vm public IP address.

The request will time out due to being blocked by Windows Firewall.

#
<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Installing-Microsoft-SQL-Server-Images/main/2.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Installing-Microsoft-SQL-Server-Images/main/3.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Installing-Microsoft-SQL-Server-Images/main/4.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Installing-Microsoft-SQL-Server-Images/main/5.png"/>

Connect to windows-vm through RDP and disable Windows Firewall as shown in the screenshots above.

#
<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Installing-Microsoft-SQL-Server-Images/main/6.png"/>

Go back to your host machine and check the ping again. It will go through now that Windows Firewall is no longer blocking it.
