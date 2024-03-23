<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>External Resources</h2>

- [Installation Files](https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
- Note - These are the all the necessary files we will need to download and install to correctly install and run this version of osTicket.


<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Deploy a virtual machine running Windows 10 OS on Azure.


<h2>Installation Steps</h2>

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/555634a1-1197-4e77-969f-d5e1990e40aa"/>
</p>
<p>
To begin, we will open up the control panel, go to programs, and click "Turn Windows features on or off". From there we will have a screen that looks like this. We will want to make sure World Wide Web Services is enabled. Then we will want to open the drop down arrow under Application Development Features and make sure "CGI" is checked. We will also want to make sure everything under Common HTTP Features is checked. Lastly under Web Management Tools we just want to make sure 'IIS Management Console" is checked. Then we can click Ok and wait for it to enable all the features. 

We will then go ahead and download and install (PHPManagerForIIS_V1.5.0.msi) and (rewrite_amd64_en-US.msi)
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/31e50325-c08f-4f0c-b4d6-2debe8ec2165"/>
</p>
<p>
Next we will create a folder in our C drive and name it PHP. Afterwards we will download (php-7.3.8-nts-Win32-VC15-x86.zip). 
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/2781526d-6720-404f-9b5c-79ff2e054e74"/>
</p>
<p>
Once we have the zip file from the last step downloaded, we will extract that file into the PHP file that we just made. Next we will download and install VC_redist.x86.exe.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/38af87c0-28f9-4dd4-a64a-58891cf2deea"/>
</p>
<p>
From here we will download mysql-5.5.62-win32.msi, and when installing we will start with the Typical setup type. Then we will make sure to launch the Configuration Wizard after installing.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/4c2f874f-b180-430b-863d-0bf3bfe1ae52"/>
</p>
<p>
When configurating, we want to make sure we choose Standard Configuration. It will then ask us for a password. We can put in whatever password we want. After going through the rest of the steps we will execute and then close the window when it's finished.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/e763b42f-8ba9-4b6f-a0e5-10cf49a2eb5c"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/9dc7aede-6acc-4178-8cde-924554b194d3"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/09dc446f-65d7-4955-bd9c-17e46a577a17"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/0f03ee08-dcba-4508-b954-917249c08c33"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/877587d7-1e52-4966-b260-537ae632b5bb"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/c2a8bc52-815a-450a-a4b0-3c4ebe5b5d70"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/d19f9d3f-05f5-40c6-baf2-21d6b596535e"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/2e04bd6f-2727-47c2-904a-4e92d8b0cb4b"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/0749420a-ebd5-42b3-ad31-163e0fd2a6aa"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


