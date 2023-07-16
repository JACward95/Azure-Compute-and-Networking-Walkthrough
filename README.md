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
4). We will name the resource group 'lab' here, but you can chose whatever you like. Then we will click create.
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
<img src="https://i.ibb.co/G2DQ6TR/take-note-of-perpetual-ping-in-wireshark.jpg"/>
</p>
<p>
38). Take a look at Wireshark and see how they just keep going. This will go on forever if we want it to. Let's take a look at how we could interrupt this process. 
</p>
<br />

<p>
<img src="https://i.ibb.co/9TrYZD6/back-in-linux-vm-go-to-networking-tab.jpg"/>
</p>
<p>
39). Go back to our normal desktop and we should still be in our Linux Vm information in Azure. Go over to Networking and click on that.  </p>
<br />

<p>
<img src="https://i.ibb.co/r6z39m9/go-to-add-inbound-port-rule.jpg"/>
</p>
<p>
40). Click on 'Add Inbound Port Rule'
</p>
<br />

<p>
<img src="https://i.ibb.co/r2jXpsT/icmp-and-deny.jpg"/>
</p>
<p>
41). Don't worry about the top portions, just click the box for ICMP and then Deny, then click Add. 
</p>
<br />

<p>
<img src="https://i.ibb.co/PQv7kRt/take-note-of-denied-access-in-cmd-and-wireshark.jpg"/>
</p>
<p>
42). Go back to our remote desktop connection and observe the results. See how the request is timing out? We just denied our Linux VM from being reached by ICMP from another IP address. 
</p>
<br />

<p>
<img src="https://i.ibb.co/09PhJcT/go-back-to-linux-vm-inbound-rule.jpg"/>
</p>
<p>
43). Now that we've observed that, go back to the normal desktop and back into the rule that we just made. 
</p>
<br />

<p>
<img src="https://i.ibb.co/FqFprZj/click-allow-and-save.jpg"/>
</p>
<p>
44). Check 'allow' and save.
</p>
<br />

<p>
<img src="https://i.ibb.co/xSzpS9q/take-note-that-it-is-back-in-working-order-for-ping.jpg"/>
</p>
<p>
45). Observe now how we have allowed communication to come back into the fold between these two machines. The requests are no longer timing out and we can see plenty of packets.
</p>
<br />

<p>
<img src="https://i.ibb.co/R7TVmPR/click-ctrl-c-to-stop-the-ping-t.jpg"/>
</p>
<p>
46). To stop this process, go into command prompt and on your keyboard hit 'Ctrl+C' to stop this pinging. 
</p>
<br />

PART C: OBSERVING SSH TRAFFIC

<p>
<img src="https://i.ibb.co/2y8xc4d/filter-for-ssh.jpg"/>
</p>
<p>
47). Go into Wireshark and like we filtered for ICMP before, we will now filter for SSH traffic.
</p>
<br />

<p>
<img src="https://i.ibb.co/9p06kRp/ssh-then-yes-then-linux-vm-password.jpg"/>
</p>
<p>
48). Go into the command prompt and type 'ssh x.x.x.x' (Linux Private IP). Then type yes to SSH into the Linux machine. Now, you'll need to type in the password that we created for the Linux machine (it should be the same as windows vm if you chose to do that). 
</p>
<br />

<p>
<img src="https://i.ibb.co/tZVHTMg/take-note-you-are-in-linux-vm-ssh.jpg"/>
</p>
<p>
49). We have no successfully SSH'ed into Linux VM. 
</p>
<br />

<p>
<img src="https://i.ibb.co/prt8s8F/take-note-that-the-source-is-linux-vm.jpg"/>
</p>
<p>
50). Take note of the traffic in Wireshark. See how now the source is coming from the Linux private IP rather than the Windows VM. 
</p>
<br />

<p>
<img src="https://i.ibb.co/0tHNDsM/type-in-linux-commands.jpg"/>
</p>
<p>
51). Type in a few Linux commands like 'hostname' or 'pwd' and you can see it will work. In Wireshark as well you'll see the traffic happen from the Linux VM. 
</p>
<br />

<p>
<img src="https://i.ibb.co/5kvZP2j/exit-out-of-linux-vm.jpg"/>
</p>
<p>
52). We can now stop this by typing exit and now we are back into making commands for the Windows VM.
</p>
<br />

PART D: OBSERVE DHCP TRAFFIC

<p>
<img src="https://i.ibb.co/3sygmzC/filter-for-DHCP.jpg"/>
</p>
<p>
53). Just as before, we will go into Wireshark and filter for DHCP Traffic. 
</p>
<br />

<p>
<img src="https://i.ibb.co/cCRzmYD/ipconfig-renew.jpg"/>
</p>
<p>
54). Go into command prompt and type in 'ipconfig /renew' and observe the effects in Wireshark.
</p>
<br />

<p>
<img src="https://i.ibb.co/dprtpTC/take-note-of-new-IP.jpg"/>
</p>
<p>
55). Thanks to this protocol, we now have a new public IP address. 
</p>
<br />

PART E: OBSERVE DNS TRAFFIC

<p>
<img src="https://i.ibb.co/ssNJcWk/filter-for-dns.jpg"/>
</p>
<p>
56). Same as before, we will now filter for DNS Traffic in Wireshark. 
</p>
<br />

<p>
<img src="https://i.ibb.co/YQWKW3m/nslookup-for-google.jpg"/>
</p>
<p>
57). Go into command prompt and type in 'nslookup www.google.com' or whatever popular website of your choosing. Observe the results and see that we can see the Public IP address of this website. 
</p>
<br />

<p>
<img src="https://i.ibb.co/qpgwfMK/take-note-of-nslookup-wireshark-data.jpg"/>
</p>
<p>
58). The same goes for Wireshark, see how the packets were sent for DNS, and if you scroll over you can see the website you chose in the detailed information as well. 
</p>
<br />

PART F: OBSERVE RDP TRAFFIC

<p>
<img src="https://i.ibb.co/7njK7Sv/filter-for-RDP-and-take-note-of-neverending-traffic.jpg"/>
</p>
<p>
59). Same as before, go into Wireshark and filter for RDP traffic by typing 'tcp.port==3389'. Now take note of the traffic. It is constantly happening without is doing anything. This is because this port shows constant live traffic between two computers. 
</p>
<br />

PART G: CLEAN UP YOUR AZURE AND DELETE RESOURCES

<p>
<img src="https://i.ibb.co/KD51C7r/close-out-of-WINVM.jpg"/>
</p>
<p>
60). Click out of the Remote Desktop Connection. 
</p>
<br />

<p>
<img src="https://i.ibb.co/mhYRRQt/go-back-to-portal-and-go-to-lab-RG.jpg"/>
</p>
<p>
61). At the main portal page, go to the lab Resource group we created. 
</p>
<br />

<p>
<img src="https://i.ibb.co/6sHF7pZ/delete-resource-group.jpg"/>
</p>
<p>
62). Click on Delete Resource Group.
</p>
<br />

<p>
<img src="https://i.ibb.co/k1YKpzH/apply-force-delete-and-delete.jpg"/>
</p>
<p>
63). Be sure to check that box at the bottom so this also takes care of your virtual machines. Type the name of the resource group and delete. 
</p>
<br />

<p>
<img src="https://i.ibb.co/0sX2b93/hooray-we-re-done.jpg"/>
</p>
<p>
64). Wait for to delete just to be sure. Now we are finished! Thank you for taking the time to read this walkthrough and I hope it was in some way helpful to you. 
</p>
<br />
