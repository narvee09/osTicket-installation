# osTicket-installation

<div align=center>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/osTicket%20splash.png">
</div>

<h2>Technologies</h2> <!---think about how well this tracks in ATS for resume, also think about making it all encompassing--->

-  Windows 10
-  Internet Information Services (IIS)
-  HeidiSQL
-  mySQL


<h2>Prerequisites</h2>
<br>
<div>
 All of the following must be installed.
</div>
- <b>PHP Manager</b>
- <b>IIS URL Rewrite Module </b>
- <b>HeidiSQL</b>
- <b>osTicket configuration files</b>
- <b>mySQL</b>

<h2>mySQL Configuration</h2>
<br>
<div>
There are a few additional steps during mySQL installation, choose typical and launch the configuration wizard.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti1.JPG" width=500 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti2.JPG" width=500 >
</div>
<br>
<br>
<div>
Inside of the wizard choose standard configuration and create a password.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti3.JPG" width=500 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti4.JPG" width=500 >
</div>
<br>
<br>
<div>
<!---optional include security setting img()--->
If you recieve this error you must navigate to the directory that holds the mySQLInstanceConfig.exe which should be in the file path C:// Program Files (x86) / MySQL / MySQL Server 5.5 / bin /
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/error%20img/error1.JPG" width=700 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/error%20img/error2.JPG" height=200 > 
</div>
<br>
<div>
Open the .exe and you will be provided the option to remove instance. Open the Configuration wizard once more and the application of security setting will be successfully applied.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/error%20img/error3.JPG" width=500 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/error%20img/error4.JPG" width=500 >
</div>

<br>

<h2>Create Folder Architecture</h2>
<br>
<div>
Navigate to the C:/ drive folder and create a folder called "PHP"then navigate to the downloads folder and extract "php-7.38.xx.xx" contents to the PHP folder that was just created.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti5.JPG" width=600 >
</div>
<br>
<div>
Open inetpub folder then open the wwwroot folder and extract osTicket folder contents and input upload directory into wwwroot folder, rename this folder to "osTicket".
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti6.JPG" width=600 >
</div>

<br> 


<h2>Internet Information Services (IIS) Manager</h2>

<h3>IIS system preperation</h3>
<br>
<div>
Navigate to control panel, programs, turn on windows featrues on or off. Once open selet internet information services, expand world wide web services, expand application developmetn and enable CGI.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti7.JPG" width=500 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti8.JPG" width=500 > 
<!---highlight selections in editing--->
</div>

<br>

<h3>IIS Configuration</h3>
<br>
<div>
Click on start then navigate to Internet Information Services (IIS) and run it as administrator. In the Connection tree Home click on PHP Manager then register new PHP. Navigate into PHP folder and select "php-cgi.exe" and click restart.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti9.JPG" width=500 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti10.JPG" width=500 >
</div>
<!---highlight "register new PHP version"--->
<br>
<div>
Click on the expansion arrow within the conection tree > sites > Default web site > osTicket and click on browse*:80(http) to confirm osTicket has been registered, the browser will open to show the osTicket installer.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti11.JPG" width=600 > 
<!--<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti12.JPG" width=600 >--->
</div>
<br>
<div>
Navigate back to the inital tree home  PHP Mangaer > Enable or disable an extension and enable:
 
 - <b>php_imap.dll</b>
-  <b>php_opcache.dll</b>
-  <b>php_intl.dll</b>
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti13.JPG" width=600 > 
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti14.JPG" height=400 >
<!---highlight in editing--->
</div>
<br>
<div>
Navigate  back to home, restart (IIS) and refresh osTicket in browser.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti15.JPG" width=600 > 
</div>

<br>

<h2>Implentation <!---and clean up---></h2>

<h3>osTicket Security Release</h3>
<br>
<div>
Intially to make sure installtion runs smoothly and osTicket is able to parse files in the C:/ permissions must be open. Navigate to wwwroot, osTicket then the include file.
</div>
<br>
<div>

</div>
<br>
<div>
Rename ost-sampleconfig.php to "ost-config.php". Open properties on this file
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti16.JPG" width=600 >
</div>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti17.JPG" width=300 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti18.JPG" width=600 > 
</div>
<br>
<div>
 Navigate to the security tab, click on advanced, disable inheritance, remove all inherited permissions from this object then click on add>select a principal. Type in "everyone" and click on check names and check Full controll then apply for now.
</div>
<br>
<div> 
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti19.JPG" width=300 > 
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti20.JPG" width=300 > 
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti21.JPG" width=300 > 
</div>

<br>

<h3>HeidiSQL</h3>
<br>
<div>
 Open HeidiSQL click on new and input the password created during the mySQL standard configuration.Right click within the unnamed tree then create new database and input the name "osTicket"  
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti22.JPG" width=500 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti23.JPG" width=500 >
</div>

<br>

<h3>OsTicket Installation</h3>
<br>
<div>
Navigate to the osTicket browser window and click continue. In the password section use the same password used in mySQL and HeidiSQL configuration, then click on install now.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti24.JPG" width=500 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti25.JPG" width=500 >
</div>

<br>

<h3>osTicket Security Lock</h3>
<br>
<div>
Navigate to wwwroot folder, osTicket, ost-config.php, properties, security, advanced, edit to change permissions.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti26.JPG" width=400>
</div>
<br>
<div>
Confirm everything is working by loggining in with creadentials created during osTicket basic installation.
</div>
<br>
<div>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti27.JPG" width=500 >
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti28.JPG" width=500 >
</div>
<br>
<br>
<br>
