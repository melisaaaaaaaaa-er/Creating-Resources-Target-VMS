# Creating Resources - Target VMs

<h2>Purpose</h2>

- Set up a Windows and Linux virtual machine.
- Configure inbound rule on their respective network security groups (NSGs) to allow all traffic from the Internet.

#
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
Change NSG Inbound Rule: Allow All Traffic

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Creating-Resources-Target-VMS-Images/main/3.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Creating-Resources-Target-VMS-Images/main/4.png"/>

Navigate to the network settings of windows-vm, scroll down to the Network Security Group configurations.

Delete the default inbound port rule.

Create a new port rule allowing all inbound traffic. This will allow all traffic from the Internet to the VM. 

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/Creating-Resources-Target-VMS-Images/main/5.png"/>

Repeat the same steps for linux-vm.
