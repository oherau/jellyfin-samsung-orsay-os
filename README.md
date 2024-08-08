# Jellyfin for Samsung Smart TV with Orsay OS
This is a version of Jellyfin for Samsung Smart TV produced before 2014.
The models concerned are using Orsay OS, a legacy operating system that is no more supported.
Apps and OS updates are no more available but the system is still customizable using the developer account.

If your TV model is newer, it is probably using Tizen OS. 
In this case you should use this software: https://github.com/jellyfin/jellyfin-tizen

# Supported Devices
Samsung TV's, Blu-ray Disk Players and Home Theatre Systems with older "Orsay" SmartHub operating system.
Specifically: D-Series (2011), E-Series (2012), F-Series (2013), H-Series (2014) plus some entry level J and K series models which still have Orsay.

The model ID can usually be found in the "Settings" menu, section "Support", "About"
You can refer to this article to understand the model naming:
https://www.samsung.com/us/support/answer/ANS00087664

If you still don't know what series TV you have, please see the below link:
https://developer.samsung.com/tv/develop/specifications/tv-model-groups



-----------------
Pre-Install steps
-----------------

Before install, a local "app store" must be set up on a local machine

Windows:
- Install "Internet Information Services" (IIS) available in Windows additionnal softwares
- Open a powershell, type ipconfig
- Write down the local IP of your machine (xxx.xxx.xxx.xxx) as you will need it during the install procedure as the ">Local app store's IP address"
- Download the jellyfin.xxx.zip and widgetlist.xml
- Copy widgetlist.xml at the root of the folder: "c:\inetpub\wwwroot"
- Copy jellyfin.xxx.zip in a new subfolder named Widgets: "c:\inetpub\wwwroot\Widgets"
- Edit the widgetlist.xml file and change the IP address to your Local IP address <download>http://192.168.1.26/Widgets/Jellyfin_2.2.6_Europe_20230928.zip</download> to <download>http://LocalIPaddress/Widgets/Jellyfin_2.2.6_Europe_20230928.zip</download>
- Make sure files are available, open a web browser and type: http://localhost/widgetlist.xml

MacOS or Linux:
- Get Local IP address (e.g. using ifconfig Terminal command)
- Download the jellyfin.xxx.zip and widgetlist.xml 
- Create a directory under your Home directory called jellyfin (e.g. /User/YourName/jellyfin)
- Copy widgetlist.xml at the root of the directory:
- Create another directory under jellyfin called Widgets (e.g. /User/YourName/jellyfin/Widgets)
- Copy the jellyfin.xxx.zip file to the Widgets folder (e.g. /User/YourName/jellyfin/Widgets/Jellyfin_2.2.6_Europe_20230928.zip)
- Edit the widgetlist.xml file and change the IP address to your Local IP address <download>http://192.168.1.26/Widgets/Jellyfin_2.2.6_Europe_20230928.zip</download> to <download>http://LocalIPaddress/Widgets/Jellyfin_2.2.6_Europe_20230928.zip</download>
- Start the Terminal App and goto the jellyfin directory (e.g. cd /User/YourName/jellyfin)
- Start a temporary web server using PYTHON using the following command:python -m SimpleHTTPServer 80
- Go to your TV and install the Jellyfin App using your MacOS's IP address (detailed instructions below)
- When complete, stop the temporary web server on your Mac by entering Control-C on the terminal.

------------------
Post-Install notes
------------------

The switch to developer mode is a mandatory step to install the software from a custom apps provider.
Some features are disabled in this mode.
Once the install is successful, you should logout from the developer account, and login with your previous regular account.
  

---------------------
2011 D-Series Install
---------------------

- On the Samsung device load up the Smart Hub and press red to login
- Login with the details "develop", password "000000"
- Once logged in, press the blue button and there should be a developer menu.
- In there select "Setting Server IP" and it will ask for an IP address. Enter  the Local app store IP address
- Once that's done select "User Application Synchronization" and hopefully it will connect and download the app to the TV.

---------------------
2012 E-Series Install
---------------------

To login as developer

- Open the Smart Hub
- Press "Tools" on the remote
- Select "Login"
- Select "Samsung account"
- Enter "develop" as your Samsung Account ID
- Enter "000000" in the Password field
- Press Login. develop should now show in the bottom left of the SmartHub screen as being logged in

To install/update the app

- Open the Smart Hub
- Confirm that you are logged in as "develop"
- Press "Tools" on the remote
- Select "Settings"
- Select "Development". If this menu option is missing then you are not logged in as "develop"
- Check the box to "Agree" to the "Terms of Service Agreement"
- Select "OK"
- Select "Setting Server IP"
- Enter the Local app store IP Address
- Select "User Application Synchronisation" - this will download the app
- Once the app has downloaded it will appear on the SmartHub screen
- Select the App
- You will then have to enter your Jellyfin's IP address and port number.

---------------------
2013 F-Series Install
---------------------

- Open the main menu and scroll down to "Smart Features" and press enter
- Select "Samsung Account"
- Select "Log In"
- In the Email field enter "develop" - no need to enter a password (the password field is inaccessible)
- Press Login
- Exit from the menu
- Press the Smart Hub button on the remote and scroll to Apps
- Select "More Apps" (at the bottom of the screen)
- Select "Options" at the top right
- Select "IP Setting"
- Enter the Local app store IP address
- Exit and then select "Start App Sync" from the Options menu - this will download the app
- Once the app has downloaded it will appear on the "More Apps" screen
- Select the App
- You will then have to enter your Jellyfin's IP address and port number (these are visible on the server's settings page).

------------------------------------------
2014 H-Series Plus Selected J and K Series
------------------------------------------

Supported models: All H and HU (4K) series models plus J4300, J5200, J5300, J6200 and K8500.

- You can logon as develop (user "develop", password "000000" or blank for some models) by clicking the menu button and than select Smart Hub and in there Samsung Account menu on your remote.
- After you logged on as develop you can press the smart hub button on your remote.
- Go to my app's list and on one of the installed apps hold the enter button down for a few seconds.
- Another window will pop up giving you the option to add the IP address. Enter the Local app store IP address.
- Afterwards hold the enter button down to go in the options again and choose "Start User app sync".
- There will pop up a new window which says "user apps sync is requested"
- After a few seconds the app will be installed on your TV.






