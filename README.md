<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation and Setup</h1>
This tutorial outlines the installation and setup of the open-source help desk ticketing system osTicket.<br/>

<h2>Environments and Technologies used</h2>

- Windows 10 (21H2)
- Internet Informatino Services (IIS)
- osTicket ticketing system


<h2>Installation Steps</h2>

<p>
  -Download the osTicket installation files <a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD" target="_blank" rel="noopener noreferrer">Here</a> and unzip the files ("osTicket-Installation-Files").
</p>
<p><img src="https://github.com/user-attachments/assets/fb3f47ce-fe59-4572-96d4-b69f6b60990a"/></p>

<p>
  -Open the Control Panel and select/click "Uninstall a program" under "Programs". On the left-hand side of the window click on "Turn Windows Features on or off"
</p>
<p><img src="https://github.com/user-attachments/assets/20e7f29e-a017-4c82-b94a-2b62c09667ce"/></p>
<br>

<p>
  -In the Windoes Features window, check and expand "Internet Information Services". Expand (double check the box is checked as well) "World Wide Web Services". Check and expand "Application Development Features". Check the "CGI" box, and then click OK.
</p>
<p><img src="https://github.com/user-attachments/assets/a5d09b60-2ee2-4aed-ac0b-56c20ef9b8b6"/></p>
<br>

<p>
  -Windows will ask you to reboot your computer. Go ahead and reboot your computer. After your computer reboots, you should now have the new folder and directory inside the C: drive ("C:\inetpub\wwwroot")
</p>
<p><img src="https://github.com/user-attachments/assets/804bd457-e494-4eb4-83c7-90f5957a82d5"/></p>
<p></p>

<p>
  -From the "osTicket-Installation-Files" folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<p>
  -From the "osTicket-Installation-Files" folder install the Rewrite Module (rewrite_amd64_en-US.msi)
</p>

<p>
  -Inside the C: drive create a "PHP" folder
</p>
<p>
  <img src="https://github.com/user-attachments/assets/5172b3c9-d5b8-4c6c-afe6-0d04a97abe0d"/>
</p>

<p>
  -From the "osTicket-Installation-Files" folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<p>
  <img src="https://github.com/user-attachments/assets/e0a8fef8-2410-4d63-aa29-953199b7926a"/>
</p>

<p>
  -From the "osTicket-Installation-Files" folder, install VC_redist.x86.exe
</p>

<p>
  -From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
</p>
<p>
  -Select "Typical" setup
</p>
<p>
  <img src="https://github.com/user-attachments/assets/1de39458-ecb2-491f-9b8d-873651e3af71"/>
</p>

<p>
  -On the last screen of the installation, select/check the "Launch the MySQL Instance Configuration Wizard" box and click "Finish"
</p>
<p>
  <img src="https://github.com/user-attachments/assets/779c41d0-9d48-49be-b966-e3ac1b9e0f6c"/>
</p>

<p>
  -In the "MySQL Server Instance Configuration" Installation window, select "Standard Configuration" and click Next.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/722255a5-ebe5-457f-b75d-38a4d13a9294"/>
</p>

<p>
  -In the "Please set the security options" installation window, type "root" for both "New root password" and "Confirm", and click Next.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/52c98292-5878-42d3-b2ad-1975a81167e9"/>
</p>

<p>
  -In the next window "Ready to execute ...", click Execute and wait for the installation to finish.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/88551d85-4056-4073-b0b9-cb8c32c6280f"/>
</p>

<p>
  -Open the Internet Information Services (IIS) Manager as Administrator
</p>
<p>
  <img src="https://github.com/user-attachments/assets/05585fe9-5f61-4b1d-b7ef-2770c2390010"/>
</p>

<p>
  -Double click and open PHP Manager.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/4ea9071f-72c3-49c5-a57c-b4d240415769"/>
</p>

<p>
  -Click on "Register new PHP version".
</p>
<p>
  <img src="https://github.com/user-attachments/assets/1b6e028d-ae40-4cde-9128-d0de64c7ef28"/>
</p>

<p>
  -Click the "..." button and select the "php-cgi.exe" file inside the C:\PHP\ directory ("C:\PHP\php-cgi.exe"), and click OK.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/7264ce88-eadb-4d47-97f9-3c78b2af2f75"/>
</p>

<p>
  -In the IIS Window Stop And Start the server by pressing "Stop", wait a couple of seconds for the sever to stop, and then click "Start".
</p>
<p>
  <img src="https://github.com/user-attachments/assets/28e0c276-85fd-44df-8dcf-986c65bb2e55"/>
  <img src="https://github.com/user-attachments/assets/8714c2c7-9ec5-4bcc-be95-5bf418a86a16"/>
</p>

<p>
  -From the "osTicket-Installation-Files" folder, unzip the "osTicket-v1.15.8.zip" and copy the "upload" folder into "C:\inetpub\wwwroot" folder/directory.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/2e546d59-9c10-484e-9630-55c1943cd3c2"/>
</p>

<p>
  -Within the "C:\inetpub\wwwroot" directory, Rename "upload" to "osTicket"
</p>
<p>
  <img src="https://github.com/user-attachments/assets/2caaf826-e513-43e6-b820-ec8eee1b3cc6"/>
</p>

<p>
  -Open the Internet Information Services (IIS) Manager as Administrator (if not open already). Stop and Start the Server
</p>
<p>
  <img src="https://github.com/user-attachments/assets/28e0c276-85fd-44df-8dcf-986c65bb2e55"/>
  <img src="https://github.com/user-attachments/assets/8714c2c7-9ec5-4bcc-be95-5bf418a86a16"/>
</p>

<p>
  -On the Internet Information Services (IIS) Manager window, on the left-hand side, expand "Sites" --> "Default Web Site" --> and click the "osTicket" folder. On the right side of the window click the "Browse 80 (http)" link. This will open the osTicket site.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/d1200998-0a74-4dff-bf48-8497de1d0075"/>
  <img src="https://github.com/user-attachments/assets/6bd34533-0523-4552-8274-3451448398ae"/>
</p>

<p>
  -On the Internet Information Services (IIS) Manager window, click on the "osTicket" folder, and double click the PHP Manager icon
</p>
<p>
  <img src="https://github.com/user-attachments/assets/2ffb4d55-42d5-4579-b570-555415c3fb9a"/>
</p>

<p>
  -Under "PHP Extensions" click the "Enable or disable an extension" link.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/111dbc17-d935-4bff-8cd5-8aaebe5c5e91"/>
</p>

<p>
  -Enable the following extensions: "php_imap.dll", "php_intl.dll", and "php_opcache.dll". Enable each extension by right-clicking on the extension and selection "Enable".
</p>
<p>
  <img src="https://github.com/user-attachments/assets/3476f6fa-27d5-427f-9622-e2aed45fb737"/>
  <img src="https://github.com/user-attachments/assets/ec0e9d98-c09c-451b-892e-50e4721155c1"/>
  <img src="https://github.com/user-attachments/assets/b58609b8-3380-4143-bef9-4526790f3caf"/>
</p>

<p>
  -Refresh the osTicket site
</p>
<p>
  <img src="https://github.com/user-attachments/assets/9c49a668-99ac-44ef-8599-deb2d9386f30"/>
</p>

<p>
  -Open the "C:\inetpub\wwwroot\osTicket\include\" directory and rename the file "ost-sampleconfig.php" to "ost-config.php"
</p>
<p>
  <img src="https://github.com/user-attachments/assets/e0a13acf-307b-46d2-bbf1-4854f5701dea"/>
  <img src="https://github.com/user-attachments/assets/5be9c0f1-9da2-4bd6-935d-ceee6f0e665f"/>
</p>

<p>
  -Assign permissions to the "ost-config.php" file. Right-click on the "ost-config.php" file and select "Properties". Selct the "Security" tab, and then click the "Advanced" button.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/4d446db0-992e-46e0-8573-4222cd9aad43"/>
</p>

<p>
  -In the "Advanced Security Settings for ost-config.php" window, click the "Disable inheritance" button. In the pop-up window click the "Remove all inherited permissions from the object" option. Then click the "Add" button.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/a6fa927e-aa1a-4cf3-846d-3270572ef2d7"/>
</p>

<p>
  -In the following window, click the "Select a principal" link. In the "Enter the object name to select" textboox, type "everyone and click the "Check Names" button. Then click the "OK" button. In the following window select the "Full Control" checkbox option, and click "OK" button
</p>
<p>
  <img src="https://github.com/user-attachments/assets/733e61ae-8521-45e9-aedb-9fab58b0b4bd"/>
  <img src="https://github.com/user-attachments/assets/8621159f-c5ba-4c16-964a-7acf5dcb7219"/>
  <img src="https://github.com/user-attachments/assets/f98b3187-0f71-4405-b001-45b89c07ef1f"/>
</p>

<p>
  -Click "Apply" button and then the "OK" button. Then click "Ok" on the next window.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/238b0bd8-90c4-480e-923f-c538b562dd01"/>
</p>

<p>
  -On the osTicket site, on the bottom of the page click the "Continue" button.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/abe7dfe5-bff6-46bd-8811-6cddf6c69fd8"/>
</p>

<p>
  -Fill out the information in the osTicket Installer site. You can make up all the information. Just take note and remember the "Username" and "Password" you use.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/60efa2c1-847f-48b1-aecc-dd8078066a3c"/>
</p>

<p>
  -From the “osTicket-Installation-Files” folder, install "HeidiSQL_12.3.0.6589_Setup". Click "next", "next", "next", "next", "install", and "finish"
</p>
<p>
  <img src="https://github.com/user-attachments/assets/20c400b2-c327-45ba-ad08-c7b84baa6fa1"/>
</p>

<p>
  -In the following window just click "Skip"
</p>
<p>
  <img src="https://github.com/user-attachments/assets/09bb655c-a60f-4db7-a16a-cefdfa69fbef"/>
</p>

<p>
  -In the "Heidi Session Manager" window, click "New", then for "User" and "Password" type 'root' (for both), and then click "Open".
</p>
<p>
  <img src="https://github.com/user-attachments/assets/97f6b260-ecdd-4fa9-8ef2-6945683fc8f9"/>
</p>

<p>
  -In the following Heidi "Unnamed" window, right-click on "Unnamed" --> "Create new" --> "Database".
</p>
<p>
  <img src="https://github.com/user-attachments/assets/794bc8e1-4a32-4ddf-a7a4-699f60a75856"/>
</p>

<p>
  -In the "Create database.." pop-up window, in the "Name:" field, type "osTicket", and click "OK". A new database named "osticket" has been created in the Heidi "Unnamed" window
</p>
<p>
  <img src="https://github.com/user-attachments/assets/6d63b185-4bb9-4224-8eed-81cfdb5b5964"/>
  <img src="https://github.com/user-attachments/assets/6e6ddb0a-603f-40c3-8c03-7c7d8dd20ae1"/>
</p>

<p>
  -In the osTicket Installer site, fillout the "Database Settings" section, and click "Install Now"
</p>
<p>
  <img src="https://github.com/user-attachments/assets/dcf803ce-5ef0-4a22-8a99-9d74474ecd64"/>
</p>

<p>
  -The osTicket ticketing system has been successfully installed and setup!
</p>
<p>
  <img src="https://github.com/user-attachments/assets/c1d298d3-e174-4aec-bc27-98e51008886c"/>
</p>

<p>
  -Now it's time to log in to osTicket, using the <a href="http://localhost/osTicket/scp/login.php">Help Desk Login Page</a> ("http://localhost/osTicket/scp/login.php")
</p>
<p>
  <img src="https://github.com/user-attachments/assets/6d4a18d1-a93f-4863-80a9-d879c6c3e3f9"/>
  <img src="https://github.com/user-attachments/assets/260c49ed-b58f-470e-a98d-2eadc7de4ac0"/>
</p>

<p>
  -You can act as the end user and create a ticket using the <a href="http://localhost/osTicket/">Support Center Page</a>. ("http://localhost/osTicket/")
</p>
<p>
  <img src="https://github.com/user-attachments/assets/1c419269-6f57-4e79-9c86-c851e95eb69d"/>
</p>
