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
- Note - These are all the necessary files we will need to download and install to correctly install and run this version of osTicket.


<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Deploy a virtual machine running Windows 10 OS on Azure.


<h2>Installation Steps</h2>

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/555634a1-1197-4e77-969f-d5e1990e40aa"/>
</p>
<p>
To begin, we will open up the control panel, go to programs, and click "Turn Windows features on or off". From there we will have a screen that looks like this. We will want to make sure World Wide Web Services is enabled. Then we will want to open the drop-down arrow under Application Development Features and make sure "CGI" is checked. We will also want to make sure everything under Common HTTP Features is checked. Lastly, under Web Management Tools we just want to make sure 'IIS Management Console" is checked. Then we can click Ok and wait for it to enable all the features. 

We will then go ahead and download and install (PHPManagerForIIS_V1.5.0.msi) and (rewrite_amd64_en-US.msi)
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/31e50325-c08f-4f0c-b4d6-2debe8ec2165"/>
</p>
<p>
Next, we will create a folder in our C drive and name it PHP. Afterwards, we will download (php-7.3.8-nts-Win32-VC15-x86.zip). 
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/2781526d-6720-404f-9b5c-79ff2e054e74"/>
</p>
<p>
Once we have the zip file from the last step downloaded, we will extract that file into the PHP file that we just made. Next, we will download and install VC_redist.x86.exe.
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
When configuring, we want to make sure we choose Standard Configuration. It will then ask us for a password. We can put in whatever password we want. After going through the rest of the steps we will execute and then close the window when it's finished.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/e763b42f-8ba9-4b6f-a0e5-10cf49a2eb5c"/>
</p>
<p>
Next, we will open up the Internet Information Services (IIS) Manager, click on our server name, click PHP, and then register new PHP version. It will ask us to provide a path and we will select C:\PHP\php-cgi.exe. Then hit ok and reload the server. 
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/9dc7aede-6acc-4178-8cde-924554b194d3"/>
</p>
<p>
When we finish the last step we can install osTicket-v1.15.8.zip from our installation files. When we download we will open the osTicket folder in our downloads, then copy the file to Windows(C:)\inetpub\wwwroot. Once it is copied we will rename it "osTicket". Then we will reload IIS. 
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/09dc446f-65d7-4955-bd9c-17e46a577a17"/>
</p>
<p>
From the IIS, we will click osTicket, click the drop-down arrow on sites, click the drop-down arrow on Default Web Site, and then click on the osTicket folder. From here we will click the "Browse *.80 (http)" button on the right side. If everything was done right then osTicket will open in our default browser.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/0f03ee08-dcba-4508-b954-917249c08c33"/>
</p>
<p>
When we open osTicket in our browser we'll notice some features that aren't enabled. We will need to enable a few of these features to set up osTicket correctly. So we will go back to the previously open osTicket folder in our IIS and open the PHP Manager. We will scroll down the the bottom and click "Enable or disable an extension". Then we will enable "php_imap.dll", "php_intl.dll", and "php_opcache.dll". Once finished we can refresh the site to see that the features have now been enabled and we can press continue.
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/877587d7-1e52-4966-b260-537ae632b5bb"/>
</p>
<p>
Our next step is to rename ost-sampleconfig. So we will go to C:\inetpub\wwwroot\osTicket\include and scroll down until we find "ost-sampleconfig.php". We will simply rename it to "ost-config.php"
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/c2a8bc52-815a-450a-a4b0-3c4ebe5b5d70"/>
</p>
<p>
Now we will right-click ost-config.php and open the properties window. We will then go to advanced security and disable all inheritance. Then we will click "Add", type "Everyone", and then give them full control. Then we will press apply and close out of the window. 
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/d19f9d3f-05f5-40c6-baf2-21d6b596535e"/>
</p>
<p>
We will need to create a database for osTicket to use before we can install osTicket onto the server. So we will download and install HeidiSQL. We will create a new session with the "New" button on the bottom right. We will then see on the right side of the window our username "root" from our MySQL setup, and we will enter the password we chose and press open. We will then right-click "Unnamed" and then click "Create New", then "Database". Then we will name it "osTicket". 
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/2e04bd6f-2727-47c2-904a-4e92d8b0cb4b"/>
</p>
<p>
Now we can go back to our browser and fill out the information needed to install osTicket to the server. So we can name our Help Desk, give it a default email, create the admin user, and then enter the information for our database. The MySQL database name will be "osTicket", the username "root", and the password will be whatever we had chosen. If everything went properly then it will have successfully been installed. 
</p>
<br />

<p>
<img src=https://github.com/CSanders000/osTicket-prereqs/assets/161166823/0749420a-ebd5-42b3-ad31-163e0fd2a6aa"/>
</p>
<p>
Lastly, there is a bit of cleanup we have to do osTicket to run properly. First, we must go to C:\inetpub\wwwroot\osTicket and then delete the setup folder. The final step is to go back to C:\inetpub\wwwroot\osTicket\include\ost-config.php, open properties, advanced security settings, and change permissions to be read and execute only.  
</p>
<br />


