<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Virtual Machine Set-up (Azure)
- Remote Desktop Connection
- Instal/Enable os-Ticket dependencies in window such as IIS(Internet Infofrmation Services), Web Platform Installer, 
- Installation of os-Ticket V1.15.8
- Also 5

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/eyk99gd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, virtual machine was set-up in Azure using the free version as shown above. The virtual machine comprises of tenants, active subscription, resource groups, virtual network and subnets. Then, a remote desktop machine was then used from a client computer to connect remotely to the virtual machine that was set-up in Azure environment using its public ip address.
</p>
<br />

<p>
<img src="https://i.imgur.com/SsbrWL5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In order to successfully connect to the above remote desktop computer, same username and password that was used in setting up Azure Virtual Machine was used in a creating a new user.
</p>
<br />

<p>
<img src="https://i.imgur.com/KQuEIhJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/1a2nX8O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above pictures are Internet Information Services installation steps in windows. IIS is windows web server, as os-ticket uses web browser thus, it was required to enable IIS or instal it as a prerequisites before os-ticket installation. Notably, this IIS web server is then used to serve os web aplication on the installed computer. Also, the folder in which the installed IIS file is saved is been highlighted above.
</p>
<br />

<p>
<img src="https://i.imgur.com/bOfXH2J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above figure is a web platform installer, that was installed in remote desktop windows, and it was used in installing other bunch of softwares such as MYSQL 5.5 databse, and some simple versions of x86 php files based on os-ticket prerequisite requirements.
</p>
<br />

<p>
<img src="https://i.imgur.com/KMrXf6t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above figure is a database as previously mentioned that is required for os-ticket to function. Any password of my choice was used, and the user name is 'roo't. Also, during installation some php files was unsuccessful however, they were seperately downloaded to complete the prerequisites installation steps as shown below. These files are Microsft c++ redistributable packages and php manager.
</p>
<br />

<p>
<img src="https://i.imgur.com/e5ZzcYZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 The above figures (c++ redistributable and php manager are the downloaded files that failed previously)
</p>
<br />

<p>
<img src="https://i.imgur.com/ZAN0JYb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As shown above, the os-Ticket V1.15.8 was downloaded and extracted from the download folder. Furthermore, there is an 'upload' folder among the downloaded os-Ticket files, this folder was then copied into IIS server as shown in the below figures. Specifically, into c:\inetpub\wwwroot and then the 'upload' folder within this wwwroot was renamed as osTicket. In summary, the installed os-Ticket application was dumped into IIS server.
</p>
<p>
<img src="https://i.imgur.com/oCFUcMD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<br />
 
 <p>
<img src="https://i.imgur.com/ABuN04A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From  the above figure, the 'upload' folder from os application that was copied and dumped into IIS server was renamed as 'osTicket'. Furtheermore, from IIS   manager page on start-up menu ISS server was then reloaded to complete os integration into IIS server.
</p>
<br />

<p>
<img src="https://i.imgur.com/fMllqpn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After restarting IIS server, on the left hand side the following link was clicked site..>default..>osTicket then on the right hand side 'Browse * 80'(http) was clicked as shown above. Basically, when port 80 is entered it then open the osTicket page as shown below.
</p>
<br />

<p>
<img src="https://i.imgur.com/plCKtU5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The above is a web application that was configured using IIS on a remote desktop computer in microsoft Azure. Also, some extension were not enabled during the loading of the osTicket web application as shown above. Hence, the below figure is used to show the steps used in enabling them.
</p>
<br />

<p>
<img src="https://i.imgur.com/xg0333K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On ISS server, these steps 'Site..>Degfault..>osTicket' then double-clicked on PHP file. Lastly, the enable/disable link was clicked and the following extensions (php_imap.dll, php_intl.dll, php_opache.dll), were enabled. After enabling them all osTicket aplication browser was then refreshed on the site, which then provide the below changes to the osTRicket web application as shown below.
</p>
<br />

<p>
<img src="https://i.imgur.com/lmXkywl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This steps involves browsing on the C:Drive where osTicket is stored and search for this file and extention (C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php then rename it to C:\inetpub\wwwroot\osTicket\include\ost-config.php).
</p>
<br />

<p>
<img src="https://i.imgur.com/GDInySf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This step involves renaning ost-sampleconfig.php file to ost-config.php
</p>
<br />

<p>
<img src="https://i.imgur.com/2MLTYrH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/x4J3nLx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After renaming the file to ost-config.php permission was then assigned to it. The steps of assinging permission includes right clight on the file, then property, security, advance, disable inheritance (i.e stopping it from receiving permission from its parent folder and then create a new permission), remove all permission, then add, select principles (i.e account or person(s)), everyone, click on check name and ok, allow everyone full control, then ok and lastly, continue on the osTicket browser to see the above display ticekting page.
</p>
<br />
