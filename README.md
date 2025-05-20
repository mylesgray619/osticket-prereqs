<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Setup a Virtual Machine in Azure
- Install the osTicket requirements
- Install osTicket itself
- Do the after-installation configuration of osTicket
- Explore osTicket as a help desk professional
<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/f6gSSoT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I used Microsoft Azure to create an osTicket virtual machine within a resource group, then filled in the required information, such as using Windows 10 OS, selecting the region you are closest to, etc.
</p>
<br />

<p>
<img src="https://i.imgur.com/H4uLfxf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here within the VM (osticket-vm), I downloaded the osTicket-Installation-Files.zip and unzipped it onto my VM desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/jEErpJZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here, I'm installing/enabling IIS in Windows with CGI by going to the control panel, programs, and then clicking on Windows Features on or off. Then, expand World Wide Web services and application development features, and check the box for CGI to enable it. Lastly, apply the changes. This will install IIS with CGI support for running CGI scripts.
</p>
<br />

<p>
<img src="https://i.imgur.com/72Ngatx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I'm installing the PHP manager and rewrite module files for IIS on Windows. This will allow me to easily manage PHP on IIS and simplify the process of integrating PHP with IIS. The rewrite module allows for powerful and flexible URL manipulation.
</p>
<br />

<p>
<img src="https://i.imgur.com/sLw1zcH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here, I create a PHP folder on the Windows C disk and then extract the PHP file into the folder. This allows me to place the PHP file in a central location where IIS can access and use it for processing PHP scripts.
</p>
<br />

<p>
<img src="https://i.imgur.com/5UnINi1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I'm installing both the "VC_redist" and "MySQL" files. The VC_redist file ensures the necessary runtime libraries for running MySQL and PHP. The MySQL file, configured with a root user and password, gives me access to the MySQL database, which will be used by applications like osTicket to store and manage data.
</p>
<br />

<p>
<img src="https://i.imgur.com/HfrArUY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here, I opened IIS as an Admin to ensure I have administrator-level access to configure and manage the server. Then I clicked on register PHP, which tells IIS to use PHP for processing dynamic web pages for the osTicket. Then I stopped and restarted the server to apply the changes.
</p>
<br />

<p>
<img src="https://i.imgur.com/D7MB6U2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here I installed and extracted the osTicket file, then copied the "upload" folder into the inetpub folder, which is the root directory for IIS. By doing this, I am preparing the system to be accessible as the osTicket application.
</p>
<br />

<p>
<img src="https://i.imgur.com/ulnO37v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here, I reloaded the server and clicked on sites, default, and osTicket. On the right side, I clicked on "browse:80," which will open the osTicket site. Next, I clicked on PHP manager, enabled or disabled an extension, and enabled three PHP extensions as shown above to ensure the osTicket has the necessary functionality. Afterwards, I refreshed the osTicket site to have the latest version of the page with all the enabled extensions.
</p>
<br />

<p>
<img src="https://i.imgur.com/4Sp7R14.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here Im going into the root directory to rename the sample configuration file (ost-sampleconfig.php) that the osTicket provided on the default settings to "ost-config.php", so that the osTicket can use it as its actual configuration file. Next, I am assigning permissions to the "ost-config.php file. By doing this, I would have to disable inheritance, which would allow me to customize its access permissions and allow authorized users to modify the file.
</p>
<br />

<p>
<img src="https://i.imgur.com/TbeVY3F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Here, I continue to set up the osTicket in the browser, I next install the HeidiSQL file that allows me to connect to the "MySQL" server. This creates a new "osTicket" database.
</p>
<br />

<p>
<img src="https://i.imgur.com/lZJ9SI3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The last thing to do is finish setting up the rest of the information on the osTicket site by selecting the database, username, and password. Then congratulations its intsalled!
</p>
<br />
