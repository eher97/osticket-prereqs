<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial demonstrates on how to install osTicket in a Virtual Machine on Azure.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Internet Information Services (IIS)
- Windows Features

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
<img src="https://user-images.githubusercontent.com/92277527/215697657-35b8379f-b906-4098-a44f-7d98eec9bc8d.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Create a Resource Group on Azure. This is where we will install our Virtual Machine. Depending on your location, choose the region that fits you best.
</p>
<br />

[![Link to video](https://i.imgur.com/ERNpSe6.png)](https://www.youtube.com/watch?v=FJJc3pZPIXs)

2. Create a Virtual Machine within the RG(Resource Group) that was just created. The VM(Virtual Machine) should have the same region as the RG.

 - Create a username and password. Make sure you remember them because we are gonna need it for when we sign into the VM on the Remote Desktop Connection!
 - Next to Image, choose Windows 10 Pro, version 21H2. We are gonna use Windows 10 for our VM.
 - Next to Size, choose either 2vcpus OR 4vcpus to run the VM more faster. (You can choose 1vcpus but it's wise not to since the VM will run very slow.)
 - Click "Next" until you get to the Networking tab and once you're there, make sure that in the Virtual Network, it says "vnet" at the end of the name!
 - Once you finished, click on "Review & Create" and it should take you to a page where it shows the overview of your VM that you're gonna create. There should be a green notification at the top that says "Validation Passed" and once you see that, click on Create at the bottom and your VM should start deploying.(It takes some time to load!)
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF3.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. After the VM has been created, click on "Go to Resource" and the page should show the overview of the VM.

 - We need the public IP Address of the VM, which is located on the right side, third row. Copy the address.
 - After copying, go to the search bar at the bottom and type in "Remote Desktop Connection" and launch it.
 - Paste in the IP Address and click Connect.
 - It's going to ask for credentials. Click on "More Choices" and then click on "use a different account." We are going to use the login/credentials we created back in Step 2 when we were creating the VM.
 - After typing in the account, try logging in. There is gonna be a warning that pops up, stating that the identity of the remote deskop can't be verified and it will ask if you want to connect to it anyway. Click yes and you should be signing into your VM.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF4.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. After successfully signing into the VM, it should look like you're launching Windows 10 for the first time.

 - Launch Microsoft Edge. Copy this link and paste it into the URL: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 | This link brings us the list of prerequisites that is required to install osTicket.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF4.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. After successfully signing into the VM, it should look like you're launching Windows 10 for the first time.

 - Launch Microsoft Edge. Copy this link and paste it into the URL: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 | This link brings us the list of prerequisites that is required to install osTicket.
 
 
</p>
<br />
