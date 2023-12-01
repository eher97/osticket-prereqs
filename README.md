<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>How To Install osTicket</h1>
This tutorial goes in-depth on how to install osTicket, a ticketing system, into a virtual machine that we will create on Azure Cloud.<br />

<h2>Environments Used</h2>

- Microsoft Azure
- Windows 10
- Information Internet Services (IIS)

<h2>Technologies/Softwares/Services Used </h2>

- Azure Virtual Machine
- Azure Resource Group
- osTicket

<h2>List of Prerequisites</h2>

- https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

<h2>Installation Steps</h2>

<p>
<img src="https://user-images.githubusercontent.com/92277527/215697657-35b8379f-b906-4098-a44f-7d98eec9bc8d.gif" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. Create a Resource Group on Azure. This is where we will install our Virtual Machine. Depending on your location, choose the region that fits you best.
</p>
<br />

<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF2.gif" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>

2. Create a Virtual Machine within the RG(Resource Group) that was just created. The VM(Virtual Machine) should have the same region as the RG.

 - Create a username and password. Make sure you remember them because we are gonna need it for when we sign into the VM on the Remote Desktop Connection!
 - Next to Image, choose Windows 10 Pro, version 21H2. We are gonna use Windows 10 for our VM.
 - Next to Size, choose either 2vcpus OR 4vcpus to run the VM more faster. (You can choose 1vcpus but it's wise not to since the VM will run very slow.)
 - Click "Next" until you get to the Networking tab and once you're there, make sure that in the Virtual Network, it says "vnet" at the end of the name!
 - Once you finished, click on "Review & Create" and it should take you to a page where it shows the overview of your VM that you're gonna create. There should be a green notification at the top that says "Validation Passed" and once you see that, click on Create at the bottom and your VM should start deploying.(It takes some time to load!)
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF3.gif" height="60%" width="60%" alt="Disk Sanitization Steps"/>
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
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF4.gif" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. After successfully signing into the VM, it should look like you're launching Windows 10 for the first time.

 - Launch Microsoft Edge. Copy this link and paste it into the URL: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 | This link brings us the list of prerequisites that is required to install osTicket.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/control%20panel.gif" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. Before we install anything, we have to enable Internet Information Services(IIS) with CGI.

 - Go to the search bar at the bottom and look up Control Panel.
 - Click on "uninstall a program" under "Programs".
 - On the left sidebar, click on "Turn Windows Features on and off".
 - Scroll down until you find "Internet Information Services". Check the box to enable it.
 - Click on [+] next to IIS and it should open up other files under it. Click the [+] on "World Wide Web Services" and then click the [+] on Application Development Features. Scroll down until you find CGI and then check the box next to it.
 - Press OK and it should start installing IIS & CGI.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF6.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. We are finally going to install the programs/softwares that we copied and pasted in the URL of Microsoft Edge!
 
 - Download PHP Manager for IIS.
 - Once it's done downloading, click on the "File Explorer" folder at the bottom and on the left bar, click on the "Downloads" folder. Keep this folder opened because this is where the downloads are going to be at.
 - Install PHP Manager.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF20.gif" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. Download and install the Rewrite Module.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF9.1.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. For this step, we are going to create a new folder/directory for one of the prerequisites.
 
- Launch File Explorer(you can also right-click the icon and click on a random folder to open another folder window)
- On the left bar, click on the > arrow on "This PC" and it should open up other directories. Click on "Windows (C:)"
- On the top left corner, click on the folder to create a new folder (you can also press Ctrl + Shift + N to create a new folder).
-  Name the folder PHP.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF11.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. Download PHP 7.3.8.
 
 - After downloading it, instead of installing it, we're going to unzip/extract the folder into the PHP folder we created earlier.
 - To extract it, right-click on the folder and click on "Extract all"
 - For the destination, click "Browse" and on the left side, click on "Windows (C:)" and click on the PHP folder. Extract the folder into the PHP folder.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF16.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. Download VC_redist.x86
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF7.gif" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
11. Download and install MySQL_5.5.62
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF8.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. The MySQL configuration wizard will pop up after installing the program.
 
 - Click on "Standard Configuration", then keep clicking "Next" until it asks you to create a password. Create a password that you can remember because we will need it! (The username is root and then your password!)
 - Click "Next" and then "Execute". It will take a bit to install everything but once it's done, click "Finish".
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF5.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. For this step, we have to enable a new version of PHP within the Internet Information Services(IIS)

 - On the search bar at the bottom, type in IIS. Right-click it and click "Run as Administrator"
 - Click on "PHP Manager"
 - Click on "Register new PHP version"
 - It's going to ask for a new PHP so we are going to browse to our PHP folder.
 - In the PHP folder, click on "php-cgi" then press OK
 - On the left bar, we are gonna go back to the home page(where it listed PHP Manager) so click back on your VM(or whatver name you named your VM)
 - On the far right, click on "Restart" so that the the new version of PHP we registered will take effect.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF21.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Next, we are going to download the osTicket folder and after downloading the folder, we are going to extract the files into a different folder/directory.

 - Right-click the osTicket folder from the "Downloads" folder and we are going to browse through the folders.
 - Windows(C:) > inetpub > wwwroot | We are going to extract it in the "wwwroot" folder.
 - After it's done installing, there should be an "upload" folder. Right-click the folder and rename it to "osTicket".
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF22.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
15. Reload IIS and Run as Adminstrator.

- On the left, click on the v arrow next to your VM and do the same with "sites" until you see "osTicket". (VM > sites > osTicket)
- On the right, click on "Browse *:80" and osTicket should come up in the web browser.
- Notice that some extensions are disabled. We are going to enable them in the next step!
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF23.gif" height="70%" width="70%" alt="Disk Sanitization Steps"/>
</p>
<p>
16. In IIS, click on "PHP Manager"
<p>
 At the bottom, click on "Enable or Disable an extension".
 
 To enable/disable an extension, right-click on them. We are gonna look for:
<p>
 
  - php.imap.dll
  - php_intl.dll
  - php.opache.dll
 <p>
 After enabling the extensions, go back to the osTicket page and refresh the page and some of the extensions should now have a green check mark.
 <p>
 <img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF24.gif" height="45%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF12.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
17. Continue onto the next page and it's going to tell us that there's a configuration file missing.
 
 - Go to File Explorer and browse through the directories: Windows(C:) > inetpub > wwwroot > osTicket > include
 - Once you get to the "include" folder, look for "ost-sampleconfig.php". Rename the file to "ost-config.php".
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF17.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
18. We are going to change the Permissions of the "ost-config.php" file.
 
 - Right-click the file and then click on "Properties".
 - Click on the "Security" tab, and then click on "Advanced".
 - Click on "Disable Inheritance" and then choose "Remove all inherited permissions from this object".
 - Click "Add" and then select "Add a principal" at the top.
 - Type in "Everyone" in the box and then select OK.
 - Check all the boxes for the permissions and click OK. Then click on "Apply" and then "OK".
 - Continue onto the next page of osTicket.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF13.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
19. We are going to download and install the final file now
 
 - Download and install HeidiSQL
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF10.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
20. After installing HeidiSQL, we are going to create our account and database for osTicket.
 
 - Launch HeidiSQL.
 - Click on "New" on the bottom left corner.
 - Create your user and password. After that, click "open".
 - On the left window, right-click and select "Create new" and then select "database".
 - Name the database "osTicket" and then click OK.
 - Add your database information at the bottom of the osTicket page. Fill out the other blanks(admin name, email, etc and THIS IS IMPORTANT BECAUSE YOU WILL NEED THE CREDENTIALS TO SIGN INTO YOUR OSTICKET) that's above the "Database Settings".
 - Once you are done setting up, click on "Install Now".
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF19.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
21. Next, we are going to change the permissions of the "ost-config.php".
 
 - Locate the file back in the "wwwroot" folder.
 - Right-click "ost-config.php" to Properties > Security > Advanced
 - Double-click on "Everyone" and uncheck "Full control", "Modify", and "Write". Apply the settings and then click OK.
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF18.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
22. Once that is done, click on the link that is below "Your Staff Control Panel"
 
 - Sign in using the credentials you created earlier from the osTicket page when you were creating your account.
 - Congratulations! You made your own osTicket database! 
 
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF14.gif" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p
<p>
23. There is an error that's at the top of the page after signing into osTicket. We are going to delete the "setup" folder/directory for security reasons, which is located:
 
 - Windows (C:) > inetpub > wwwroot > osTicket
 - Once you find the "setup" folder, delete it.
 
</p>
<br />


<p>
<img src="https://github.com/eher97/osticket-prereqs/blob/main/GIFs/GIF15.gif" height="85%" width="85%" alt="Disk Sanitization Steps"/>
</p>
<p>
24. Refresh the osTicket page and the error at the top should disappear!
 
 
</p>
<br />


<p>
I hope the steps to install osTicket in a Virtual Machine on Azure was easy to understand.
</p>
