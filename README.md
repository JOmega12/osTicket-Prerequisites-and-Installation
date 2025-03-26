<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Prerequisites:</h2>

- Log into Azure and into the VM
- Download <a href="https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download">osTicketFiles</a>
- Enable IIS in Windows with CGI
- Install PHP manager for IIS from the <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">osTicket Installation Files</a>
- Install the Rewrite Module from the <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">osTicket Installation Files</a>
- Install VC_redistx86 from the <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">osTicket Installation Files</a>
- Install MYSQL 5.5.62 from the <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">osTicket Installation Files</a>
- Install HeidiSQL from the <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD">osTicket Installation Files</a>


<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

<h2>Install A Windows Virtual Machine </h3>

- use your own username and password that you can remember

<h2>Log into Virtual Machine</h2>

<h2>Within the osTicket VM, download this installation <a href="https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download">here</a></h2>

<h2>Enable IIS with CGI</h2>

- Open IIS as an admin
- World Wide Web Services -> Application Development Features -> [X] CGI

<h2>Register PHP from within IIS</h2>

- Within IIS install PHPManagerForIIS_V1.5.0.msi

<h2>Install Rewrite Module</h2>

- Install this file rewrite_amd64_en-US.msi

<h2>Create a new directory</h2>

- Go to PC
- Create PHP folder

<h2>Install "VC_redist.x86.exe"</h2>
  <p>Locate "php-7.3.8-nts-Win32-VC15-x86.zip" in this file</p>

<h2>Install MySQL</h2>

- Launch config Wizard
- Standard Configuration
- Username: `root`
- Password: `root`

<h2> Open IIS as an Admin</h2>


<h2> Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)</h2>



<h2>Reload IIS</h2>

- Open IIS, Stop and Start the Server


<h2> Install OSTicket</h2>

- Install osTicket from these files by unzipping it first: osTicket-v1.15.8.zip
- Within “c:\inetpub\wwwroot” rename 'upload' to `osTicket`
- Reload IIS by opening IIS and stopping and starting the server


<h2>Launch osTicket</h2>

- within IIS ->sites -> Default -> osTicket
- Double-click PHP Manager
- Click 'Enable or disable an extension'

  - Enable:
  - php_imap.dll
  - php_intl.dll
  - php_opcache.dll
- Then refresh osTicket in browser then observe changes


<h2> Rename ost-config.php </h2>

- From: `C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php`
- To: `C:\inetpub\wwwroot\osTicket\include\ost-config.php`

<h2> Assign Permissions: to `ost-config.php`</h2>

- Disable Inheritance -> Remove All
- New Permissions -> Everyone -> All


<h2>Install HeidiSQL</h2>

- Open Heidi Sql from 'osTicket-Installation-Files' folder
- Create a new session, root/root
- Connect to the session
- Create a database called `osTicket`

<h2>Set Up osTicket in the browser:</h2>

- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: root
- Click 'Install Now!'

<h2>Browse to help desk login: <a href="http://localhost/osTicket/scp/login.php">http://localhost/osTicket/scp/login.php</a></h2>

<h2>End Users osTicket: <a href="http://localhost/osTicket/">http://localhost/osTicket/</a></h2>

<h1>Congrats! You now have osTicket installed!</h1>
<br />
