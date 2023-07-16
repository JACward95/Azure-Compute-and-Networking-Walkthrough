<p align="center">
<img src="https://github.com/JACward95/ostickets-prereq/blob/main/microsoft-azure7662.jpg" alt="Azure logo"/>
</p>

<h1>Azure Compute and Networking - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation two virtual machines and how they can communicate with each other.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: Walkthrough on Azure Compute and Networking](https://www.youtube.com/watch?v=eGK_mVi5U-A)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop


<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Windows 10 OS
- Microsoft Azure Account (Free or Pay-As-You-Go)
- Internet Connection

<h2>The In Depth Walkthrough!</h2>

PART A: CREATING OUR RESOURCES IN MICROSOFT AZURE

<p>
<img src="https://i.ibb.co/bWVcGd0/portal-for-azure.jpg"/>

</p>
<p>
1). We will first start in the main portal for Microsoft Azure.
</p>
<br />

<p>
<img src="https://i.ibb.co/5T3BfLD/Resource-Group.jpg"/>
</p>
<p>
2). Click on Resource Groups.
</p>
<br />

<p>
<img src="https://i.ibb.co/rHhnbrh/Resourge-Group-Create.jpg"/>
</p>
<p>
3). Click on create to create a new Resource Group.
</p>
<br />

<p>
<img src="https://i.ibb.co/Fzdbzgj/RG-Name-and-Create.jpg"/>
</p>
<p>
4). We're going name is resource group 'lab' here, but you can chose whatever you like. Then we will click create.
</p>
<br />

<p>
<img src="https://i.ibb.co/Hp6g0RK/VM.jpg"/>
</p>
<p>
5). Go back to the main portal page for Azure and click on Virtual Machines.
</p>
<br />

<p>
<img src="https://i.ibb.co/GQ9rCDK/Create-VM.jpg"/>
</p>
<p>
6). Click on create Azure Virtual Machine.
</p>
<br />

<p>
<img src="https://i.ibb.co/XWMknYH/VM-Lab-RG.jpg"/>
</p>
<p>
7). We will choose the 'lab' resource group that we created earlier to place this Virtual Machine in. 
</p>
<br />

<p>
<img src="https://i.ibb.co/ck5t60Q/VM-Basic-Details.jpg"/>
</p>
<p>
8). Name your Windows Virtual Machine 'Windows-vm' that way we can tell it apart from the other one we will create. Choose whatever region you like. Then for image we will choose Windows 10 Pro Version. 
</p>
<br />

<p>
<img src="https://i.ibb.co/K6fr8LQ/VM-CPU-chosen.jpg"/>
</p>
<p>
9). Choose the 2 VCpus and 16 GiB memory option for size so we can operate inside this virtual machine a bit quicker. 
</p>
<br />

<p>
<img src="https://i.ibb.co/qxVf6jc/VM-username-and-pass.jpg"/>
</p>
<p>
10). Make your own username and password (password must fit parameters) but do take note of this somewhere or remember it. We will use this to log on the Virtual Machine through Remote Desktop Connection later. 
</p>
<br />

<p>
<img src="https://i.ibb.co/vhqDmVk/VM-Vnet-and-Create.jpg"/>
</p>
<p>
11). Take note of the new Virtual Network we are creating. We will need to use this for our Linux Virtual Machine here shortly. Then Review and Create. 
</p>
<br />

<p>
<img src="https://i.ibb.co/2Sv6VK1/Back-Portal-and-Wait.jpg"/>
</p>
<p>
12). Go back to the main portal page and wait for it to deploy. We do this so we do not rush into making the next Linux virtual machine and have no access to the virtual network we just created with the Windows Virtual Machine. Now repeat the steps to make a virtual machine. 
</p>
<br />

<p>
<img src="https://i.ibb.co/1vfMMQ3/Linux-VM-Name.jpg"/>
</p>
<p>
13). We will name this one 'Linux-vm'. 
</p>
<br />

<p>
<img src="https://i.ibb.co/GvQ4Gxf/Ubuntu-Server.jpg"/>
</p>
<p>
14). Choose the image to be Ubuntu Server 20.04 along with the same VCPUs and 16 GiB memory as before. 
</p>
<br />

<p>
<img src="https://i.ibb.co/Rz8RmDX/Linux-username-and-pass.jpg"/>
</p>
<p>
15). Here we will not use the SSH key and instead make a username and password for our Linux VM. Feel free use the exact same one we created for our Windows Virtual Machine.  
</p>
<br />

<p>
<img src="https://i.ibb.co/chjgLc1/Linux-VNET-and-Create.jpg"/>
</p>
<p>
16). Make sure the same virtual network we created in our Windows VM is the same as this one. Then hit Review and Create.
</p>
<br />

PART B: REMOTE DESKTOP INTO WINDOWS VIRTUAL MACHINE AND OBSERVE ICMP TRAFFIC

<p>
<img src="https://i.ibb.co/s1S3FGG/Win-VM-Remote.jpg"/>
</p>
<p>
17). Now we will go into the Windows VM we just created. 
</p>
<br />

<p>
<img src="https://i.ibb.co/h7NsK1L/Win-VM-Pub-Ip.jpg"/>
</p>
<p>
18). Copy the Public IP address.
</p>
<br />

<p>
<img src="https://i.ibb.co/b6m77ZR/Remote-Desktop-Search.jpg"/>
</p>
<p>
19). Search for 'remote desktop connection' and click on the program.
</p>
<br />

<p>
<img src="https://i.ibb.co/mC446Rj/NOte-of-Same-IP-for-Win-Vm.jpg"/>
</p>
<p>
20). Take note after you paste the IP address in there it is for sure the same one as it is on Azure.
</p>
<br />

<p>
<img src="https://i.ibb.co/pnCWy5F/More-Choices.jpg"/>
</p>
<p>
21). Go to More Choices to use a different account to log in with. 
</p>
<br />

<p>
<img src="https://i.ibb.co/P4jBYpd/different-account-and-username-and-pas-of-winvm.jpg"/>
</p>
<p>
22). Type in that username and password that we out into the Windows Virtual Machine that we created from before. 
</p>
<br />

<p>
<img src="https://i.ibb.co/G0RxZKR/just-click-yes.jpg"/>
</p>
<p>
23). Just click yes here.
</p>
<br />

<p>
<img src="https://i.ibb.co/yNhj9Sk/Win-VM-desktop-and-edge.jpg"/>
</p>
<p>
24). Wait for the connection to be successful, then you'll see some messages pop up. Just click NO for all of them and you will then be lead here at the 'desktop' for our windows virtual machine.
</p>
<br />

<p>
<img src="https://i.ibb.co/1qyxr1m/type-wire-shark-and-download.jpg"/>
</p>
<p>
25). Go to Edge and type in Wireshark, then go to download
</p>
<br />

<p>
<img src="https://i.ibb.co/DRFgcYq/download-wireshark-continue.jpg"/>
</p>
<p>
26). Click on Windows Intel Installer, then open up the folder where it downloaded. 
</p>
<br />

<p>
<img src="https://i.ibb.co/6WWsQ2v/find-wireshark-in-downloads-double-click-to-run-program.jpg"/>
</p>
<p>
27). Double click on the program once you see the logo. 
</p>
<br />

<p>
<img src="https://i.ibb.co/tH7fzzc/click-through-dialogue-boxes.jpg"/>
</p>
<p>
28). Go through the dialogue boxes, keep clicking next. Don't click on anything else except the next options, then finish installing. 
</p>
<br />

<p>
<img src="https://i.ibb.co/R0p3xLR/after-finishing-the-dowload-search-for-wire-shard-and-open.jpg"/>
</p>
<p>
29). Search for Wireshark at the search bar then click on the program. 
</p>
<br />

<p>
<img src="https://i.ibb.co/7bggLxh/type-cmd-and-open-command-propt.jpg"/>
</p>
<p>
30). Once that is open, go down to the search bar and type 'cmd' and click on command prompt to open that as well. 
</p>
<br />

<p>
<img src="https://i.ibb.co/pJ9sCZd/minimize-RDC-and-find-linux-private-ip.jpg"/>
</p>
<p>
31). We can get out of this page of the Remote Desktop Connection and back to our regular computer by clicking the minimize button.
</p>
<br />

<p>
<img src="https://i.ibb.co/Hhh13HX/back-to-portal-and-open-lixux-vm.jpg"/>
</p>
<p>
32). Go back to the portal for Azure and click on the Linux VM we made. 
</p>
<br />

<p>
<img src="https://i.ibb.co/RSx89yT/lixux-private-IP.jpg"/>
</p>
<p>
33). Copy the PRIVATE IP Address of this virtual machine.
</p>
<br />

<p>
<img src="https://i.ibb.co/5sZg0QN/back-in-WINVM-filter-for-ICMP-in-wireshark.jpg"/>
</p>
<p>
34). Now go back to the remote desktop of our Windows VM. Go to Wireshark and filter for 'ICMP' at the bar at the top. Click the little shark icon and then the forward button to enable this filter. We will now only see traffic that is caused by 'ICMP'. 
</p>
<br />

<p>
<img src="https://i.ibb.co/Zd40Dw9/ping-the-linux-private-ip-in-cmd.jpg"/>
</p>
<p>
35). Type in the command prompt 'Ping x.x.x.x' (whatever private IP address the Linux VM had for you) and hit enter. 
</p>
<br />

<p>
<img src="https://i.ibb.co/pR4Gk7q/take-note-of-what-happens-in-wireshark.jpg"/>
</p>
<p>
36). Take note of the packets in Wireshark. See how the private IP of the Windows VM is requesting the Linux VM, and the Linux Vm is replying back with its own packet. We are communicating between these two machines using ICMP. 
</p>
<br />

<p>
<img src="https://i.ibb.co/yhcmJxg/perpetual-ping.jpg"/>
</p>
<p>
37). Now, let's go back to the command prompt and perpetually ping the Linux Private IP address by typing 'Ping -t x.x.x.x' (Linux IP we used before) 
</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />
<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />

<p>
<img src=""/>
</p>
<p>

</p>
<br />







