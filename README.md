<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial demonstrates on how to install osTicket in a Virtual Machine on Azure.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
<img src="https://raw.githubusercontent.com/eher97/osticket-prereqs/main/GIFs/GIF1.gif?token=GHSAT0AAAAAAB6A6E73EOA74LBP2RFZCO7KY6YXQ7A" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Create a Resource Group on Azure. This is where we will install our Virtual Machine. Depending on your location, choose the region that fits you best so in my case, I chose US East.
</p>
<br />

<p>
<img src="https://imgur.com/a/iYdq2n2" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

[![Watch the video](https://i.imgur.com/vKb2F1B.png)](https://youtu.be/vt5fpE0bzSY)

2. Create a Virtual Machine within the RG(Resource Group) that was just created. The VM(Virtual Machine) should have the same region as the RG.

 - Create a username and password. Make sure you remember them because we are gonna need it for when we sign into the VM on the Remote Desktop Connection!
 - Next to Image, choose Windows 10 Pro, version 21H2. We are gonna use Windows 10 for our VM.
 - Next to Size, choose either 2vcpus OR 4vcpus to run the VM more faster. (You can choose 1vcpus but it's wise not to since the VM will run very slow.)
 - Click Next until you get to the Networking tab and once you're there, make sure that in the Virtual Network, it says "vnet" at the end of the name!
 - Once you finished, click on Review & Create and it should take you to a page where it shows the overview of your VM that you're gonna create. There should be a green notification at the top that says "Validation Passed" and once you see that, click on Create at the bottom and your VM should start deploying.(It takes some time to load!)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. Create a Virtual Machine within the RG(Resource Group) that was just created. The VM(Virtual Machine) should have the same region as the RG.

 - Next to Image, choose Windows 10 Pro, version 21H2. We are gonna use Windows 10 for our VM.
 - Next to Size, choose either 2vcpus OR 4vcpus to run the VM more faster. (You can choose 1vcpus but it's wise not to since the VM will run very slow.)
 - Click Next until you get to the Networking tab and once you're there, make sure that in the Virtual Network, it says "vnet" at the end of the name!
 - Once you finished checking, click on Review & Create and it should take you to a page where it shows the overview of your VM that you're gonna create. There should be a green notification at the top that says "Validation Passed" and once you see that, click on Create at the bottom and your VM should start deploying.(It takes some time!)
</p>
<br />
