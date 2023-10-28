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

<br />NOTE Make sure all Common HTTP Features are checked.

<br /> To make sure the IIS is installed / enabled go to a browser of your choice and search for 127.0.0.1 It should look something like this.

![IIS INSTALL](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/65d2a8e0-0886-40a6-9a70-5c381f2c4f9f)


</p>
<p>
5.) Now that the IIS is enabled, From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) Go through the install wizard and complete the install.

6.) Next from the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

7.) Create a folder in the C drive called PHP.

8.) From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP

<br />!! ATTENTION !! If this appears, choose to “Keep” the file:
![PHP KEEP FILE](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/72da29fb-ed97-49b3-b35a-2d2b300b1fc8)
![PHP KEEP FILE 2](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/55ed6049-e3ae-42b6-99f9-f942aaef867b)

</p>
<br />

<p>
9.) Once you have downloaded and extracted the zip file into the PHP folder on the C drive, download and install the VC_redist.x86.exe from the installation files. Go through the setup wizard to finish setting up and installing the VC_redist.x86.exe.

10.) Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) Run the setup wizard: Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration ->

Make the new root password: Password1

![MYSQL SERVER 1](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/7d11f327-ea6e-41c1-9c9f-728c964f6f4a)
<br /> Execute the process on the next page.
![MYSQL SERVER 2](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/d5467a90-11ad-4b68-8898-68ed08470017)
</p>
<p>
11.) Now that we have the files downloaded and installed we will want to search for IIS in the windows search bar. Open IIS as an administrator. The program should look like this.

![vm osticket home 1](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/c33239cf-1d59-4588-8c75-4c859357c161)

2.) We will now want to register PHP from within IIS. Click on PHP Manager
![vm osticket home 2](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/363b47a5-3b00-40ab-8cc3-0b661dd28f92)
<br />Register new PHP version.
![vm osticket home 3](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/93b866a6-069b-49cb-a1da-5f571481ba9a)
<br />You will want to provide a path to the php executable file (php-cgi.exe)). Go to C Drive -> PHP -> click on php-cgi file.
![register php](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/a7af460e-e363-47e8-a3bc-bd27de6cf3e0)
<br />Restart the IIS server.
![iis restart](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/8a8f8fa4-abb7-4238-a4bd-8512e96fc7bf)


  
</p>
<br />


<p>
  13.) Install osTicket v1.15.8 -Download osTicket from the Installation Files Folder -Extract and copy "upload" folder to c:\inetpub\wwwroot -Within c:\inetpub\root, Rename "upload" to "osTicket"

Reload IIS again.

14.) On IIS go to sites -> Default -> osTicket -On the right, click “Browse *:80”
![browse 80](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/9ec0702b-b2a4-4d46-89d0-01716aea389a)

Some extensions are not enabled on the osTicket browser.
![osticket extensions](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/9842972f-dfe3-4e77-b834-297817990390)


To enable the extensions: -Go back to IIS, sites -> Default -> osTicket -Double click PHP manager -Click "Enable or disable an extension"
![PHP MANAGER ENABLE OR DISABLE](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/f150c03e-454d-44ca-a58a-351ca168ab84)
![PHP MANAGER ENABLE OR DISABLE 2](https://github.com/codeByKelvinn/osticket-prereqs/assets/110644520/2e65d66c-f6a0-4e13-b357-2caab8eec216)



</p>
<br />


<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
