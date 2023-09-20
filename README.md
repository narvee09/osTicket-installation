# osTicket-installation

(img placeholder splash)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/osTicket%20splash.png">
<h2>Technologies</h2> <!---think about how well this tracks in ATS for resume, also think about making it all encompassing--->

-  Windows 10
-  Internet Information Services (IIS)
-  HeidiSQL
-  mySQL


<h2>Prerequisites</h2>

- <b>PHP Manager</b>
- <b>IIS URL Rewrite Module </b>
- <b>HeidiSQL</b>
- <b>mySQL</b>
- <b>osTicket configuration files</b>


<h2>mySQL Configuration</h2>

-  -  img placeholder(mySQL setup wizard)

-  -  choose typical and launch the configuration wizard
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti1.JPG" width=600 height=300> <img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti2.JPG" width=600 height=300>                          (osti1,osti2) 
-  -  Inside of the wizard choose standard configuration and create a password
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti3.JPG" width=600 height=300> <img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti4.JPG" width=600 height=300>     (osti3,osti4)


<!---optional include security setting img()--->
if you recieve this error you must navigate to the directory that holds the mySQLInstanceConfig.exe which should be in the file path C:// Program Files (x86) / MySQL / MySQL Server 5.5 / bin /
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/error%20img/error1.JPG" width=600 height=300>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/error%20img/error2.JPG" width=600 height=300> 
(img placeholder error2

Open the exe and you will be provided the option to remove instance 
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/error%20img/error3.JPG" width=600 height=300> (img placeholder error3).
Open the Configuration wizard once more and the application of security setting will be successfully applied.
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/error%20img/error4.JPG" width=600 height=300> (img placeholder error4)



<h2>Create Folder Architecture</h2>
Navigate to the C:/ drive folder and create a folder called "PHP".
- img placeholder(php folder creation screen and downloads folder extraction screen)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti5.JPG" width=600 height=300> (osti5)
Navigate to the downloads folder and extract "php-7.38...ect.ect" to the PHP folder that was just created

-  open inetpub folder

-  -  opend wwwroot folder
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti6.JPG" width=600 height=300> (osti6)
-  -  extract osTicket folder contents and input upload directory into wwwroot folder, rename this folder to "osTicket"
 


<h2>Internet Information Services (IIS) Manager</h2>

<h3>IIS system preperation</h3>
Navigate to control panel > programs > turn on windows featrues on or off 
img placeholder(control panel with selection images)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti7.JPG" width=600 height=300> (osti7)
internet information services > expand world wide web services > expand application developmetn > enable CGI
<!---highlight selections in editing--->
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti8.JPG" width=600 height=300> (osti8)
img placeholder(IIS navigation screens, include connection tree expansion)

Click on start then navigate to IIS and run it as administrator.

In the Connection tree Home click on PHP Manager then register new PHP. Navigate into PHP folder and select "php-cgi.exe" and click restart.
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti9.JPG" width=600 height=300>  <img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti10.JPG" width=600 height=300> (osti9, osti10)
<!---highlight "register new PHP version"--->


Click on the expansion arrow within the conection tree > sites > Default web site > osTicket and click on browse*:80(http) to confirm osTicket has been registered.
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti11.JPG" width=600 height=300>  <img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti12.JPG" width=600 height=300> (osti11,osti12)

Navigate back to the inital tree home  PHP Mangaer > Enable or disable an extension and enable:
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti13.JPG" width=600 height=300> <img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti14.JPG" width=600 height=300>  (osti13,osti14)
<!---highlight in editing--->
-  php_imap.dll
-  php_opcache.dll
-  php_intl.dll

Navigate to home, restart (IIS) and refresh osTicket in browser (img placeholder to show extension update[how it should look])
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti15.JPG" width=600 height=300> (osti15)


<h2>Implentation <!---and clean up---></h2>
<h3>osTicket Security Release</h3>
Navigate to wwwroot>osTicket>include 
img(placeholder)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti16.JPG" width=600 height=300> (osti16)
Rename ost-sampleconfig.php to "ost-config.php". Open properties on this file
imgplaceholder(ost-congig.php properties screens)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti17.JPG" width=600 height=300>
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti18.JPG" width=600 height=300> 
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti19.JPG" width=600 height=300> 
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti20.JPG" width=600 height=300> (osti17-osti21)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti21.JPG" width=600 height=300> 
Navigate to the security tab>advanced>disable inheritance>remove all inherited permissions from this object then click on add>select a principal>type in "everyone" and click on check names and check Full controll then apply for now.

<h3>HeidiSQL</h3>
img(placeholder h-SQL screens)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti22.JPG" width=600 height=300> <img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti23.JPG" width=600 height=300>(osti22-osti23)
Open HeidiSQL click on new and input the password created during the mySQL standard configuration.
Right click within the unnamed tree then create new > database and input the name "osTicket"  

<h3>OsTicket Installation</h3>
Navigate to the osTicket browser window and click continue
img placeholder(osTicket basic installation *blank* screen)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti24.JPG" width=600 height=300>  <img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti25.JPG" width=600 height=300> (osti24,osti25)
In the password section use the same password used in mySQL and HeidiSQL configuration, then click on install now

<h3>osTicket Security Lock</h3>
Navigate to wwwroot folder> osTicket>ost-config.php>properties>security>advanced>edit to change permissions
img placeholder (to show finsihed permissions settings[read & execute/read])
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti26.JPG" width=600 height=300> (osti26)

img place holder( of osTicket login screen)
<img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti27.JPG" width=600 height=300>  <img src="https://github.com/narvee09/IT-images/blob/main/Basic%20IT/osTicket/install/osti28.JPG" width=600 height=300> (osti27,osti28)
Confirm everything is working by loggining in with creadentials created during osTicket basic installation.
