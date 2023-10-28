<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable IIS
- Install Web Platform Installer
- Install MySQL
- Install C++ Redistribute Rule
- Configure Permissions

<h2>Installation Steps</h2>

<p>
1.) The first thing you are going to want to do is create a virtual machine by going to https://portal.azure.com/. Setup your virtual machine with Windows 10 Pro, version 22H2. Note, you will want to create a virtual machine with atleast 2 vcpus and 16 gbs of memory.

2.) Once you have created your virtual machine you will want to conncet to it by using the public ip address the vm is setup with. You will connect using the remote desktop connection app.
  ![vm image](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/5aa77554-bebc-43c0-be9a-68ec1edfd03f)
  ![remote desktop image](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/33c3aaee-022e-40d3-8e75-4a34a19522c3)

</p>
<p>


3.) Once you have connected to your virtual machine you will want to go to your control panel. From the control panel open up programs. Select, Turn Windows features on and off.
![windows - programs images](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/6f25089a-ae30-42d2-a38f-681a7cc0ea7c)
![windows - programs images 2](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/8de18f83-f254-46c6-be7e-0e34392a731c)


</p>
<br />

<p>

  4.) You will want to install / enable IIS in Windows with CGI and Common HTTP Features

World Wide Web Services -> Application Development Features -> [X] CGI [X] Common HTTP Features
![Windows with CGI and Common HTTP Features 1](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/2766e8ca-d9fe-4e12-9fa2-1ab6ffa864b4)

![Windows with CGI and Common HTTP Features 2](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/464b9551-df70-4463-a8f3-7e9500f680ad)

</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
