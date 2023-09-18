# osTicket-installation

(img placeholder splash)

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

-  -  choose typical and launch the configuration wizard                          (osti1,osti2) 
-  -  Inside of the wizard choose standard configuration and create a password    (osti3,osti4)
<!---optional include security setting img()--->
<!---if you recieve this error you must navigate to the directory that holds the mySQLInstanceConfig.exe which should be in the file path C:// Program Files (x86) / MySQL / MySQL Server 5.5 / bin /(img placeholder error2)--->
<!---Open the exe and you will be provided the option to remove instance (img placeholder error3). Open the Configuration wizard once more and the application of security setting will be successfully applied.(img placeholder error4)--->



<h2>Create Folder Architecture</h2>
Navigate to the C:/ drive folder and create a folder called "PHP".
- img placeholder(php folder creation screen and downloads folder extraction screen)  (osti5)
Navigate to the downloads folder and extract "php-7.38...ect.ect" to the PHP folder that was just created

-  open inetpub folder

-  -  opend wwwroot folder                                                           (osti6)
-  -  extract osTicket folder contents and input upload directory into wwwroot folder, rename this folder to "osTicket"
 


<h2>Internet Information Services (IIS) Manager</h2>

<h3>IIS system preperation</h3>
Navigate to control panel > programs > turn on windows featrues on or off 
img placeholder(control panel with selection images)                                 (osti7)
internet information services > expand world wide web services > expand application developmetn > enable CGI
<!---highlight selections in editing--->                                             (osti8)
img placeholder(IIS navigation screens, include connection tree expansion)

Click on start then navigate to IIS and run it as administrator.

In the Connection tree Home click on PHP Manager then register new PHP. Navigate into PHP folder and select "php-cgi.exe" and click restart.                                                         (osti9, osti10)
<!---highlight "register new PHP version"--->


Click on the expansion arrow within the conection tree > sites > Default web site > osTicket and click on browse*:80(http) to confirm osTicket has been registered.                          (osti11,osti12)

Navigate back to the inital tree home  PHP Mangaer > Enable or disable an extension and enable:   (osti13,osti14)
<!---highlight in editing--->
-  php_imap.dll
-  php_opcache.dll
-  php_intl.dll

Navigate to home, restart (IIS) and refresh osTicket in browser (img placeholder to show extension update[how it should look])                                                                                        (osti15)


<h2>Implentation <!---and clean up---></h2>
<h3>osTicket Security Release</h3>
Navigate to wwwroot>osTicket>include 
img(placeholder)                                                                                      (osti16)
Rename ost-sampleconfig.php to "ost-config.php". Open properties on this file
imgplaceholder(ost-congig.php properties screens)                                                (osti17-osti21)
Navigate to the security tab>advanced>disable inheritance>remove all inherited permissions from this object then click on add>select a principal>type in "everyone" and click on check names and check Full controll then apply for now.

<h3>HeidiSQL</h3>
img(placeholder h-SQL screens)                                                                      (osti22-osti23)
Open HeidiSQL click on new and input the password created during the mySQL standard configuration.
Right click within the unnamed tree then create new > database and input the name "osTicket"  

<h3>OsTicket Installation</h3>
Navigate to the osTicket browser window and click continue
img placeholder(osTicket basic installation *blank* screen)                                           (osti24,osti25)
In the password section use the same password used in mySQL and HeidiSQL configuration, then click on install now

<h3>osTicket Security Lock</h3>
Navigate to wwwroot folder> osTicket>ost-config.php>properties>security>advanced>edit to change permissions
img placeholder (to show finsihed permissions settings[read & execute/read])                          (osti26)

img place holder( of osTicket login screen)                                                     (osti27,osti28)
Confirm everything is working by loggining in with creadentials created during osTicket basic installation.
