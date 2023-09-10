# osTicket-installation


<h1>system requirements</h1>

<h2>Download</h2>
-  <b>Download and install PHP Manager</b>

-  <b>Download and install rewrite_amd64_en-US</b>

-  <b>Download and install HeidiSQL</b>

-  <b>Download and install mySQL</b>

-  -  img placeholder(mySQL setup wizard)

-  -  choose typical and launch the configuration wizard
-  -  Inside of the wizard choose standard configuration and create a password


<h2>Create Folder Architecture</h2>
Navigate to the C:/ drive folder and create a folder called "PHP".
- img placeholder(php folder creation screen and downloads folder extraction screen)
Navigate to the downloads folder and extract "php-7.38...ect.ect" to the PHP folder that was just created

-  open inetpub folder

-  -  opend wwwroot folder
-  -  extract osTicket folder contents and input upload directory into wwwroot folder, rename this folder to "osTicket"
 


<h2>Internet Information Services (IIS) Manager</h2>

img placeholder(IIS navigation screens, include connection tree expansion)

Click on start then navigate to IIS and run it as administrator.

In the Connection tree Home click on PHP Manager then register new PHP. Navigate into PHP folder and select "php-cgi.exe" and click restart.

Click on the expansion arrow within the conection tree > sites > Default web site > osTicket and click on browse*:80(http) to confirm osTicket has been registered.

Navigate back to the iinital tree home > PHP Mangaer > Enable or disable an extension and enable:

-  php_imap.dll
-  php_opcache.dll
-  php_intl.dll

Navigate to home, restart (IIS) and refresh osTicket in browser (img placeholder to show extension update[how it should look])


<h2>Implentation and clean up</h2>
<h3>osTicket Security Release</h3>
Navigate to wwwroot>osTicket>include 
img(placeholder)
Rename ost-sampleconfig.php to "ost-config.php". Open properties on this file
imgplaceholder(ost-congig.php properties screens)
Navigate to the security tab>advanced>disable inheritance>remove all inherited permissions from this object then click on add>select a principal>type in "everyone" and click on check names

<h3>HeidiSQL</h3>
img(placeholder h-SQL screens)
Open HeidiSQL click on new and input the password created during the mySQL standard configuration.
Right click within the unnamed tree then create new > database and input the name "osTicket"

<h3>OsTicket Installation</h3>
Navigate to the osTicket browser window and click continue
img placeholder(osTicket basic installation *blank* screen)
In the password section use the same password used in mySQL and HeidiSQL configuration, then click on install now

<h3>osTicket Security Lock</h3>
Navigate to wwwroot folder> osTicket>ost-config.php>properties>security>advanced>edit to change permissions
img placeholder (to show finsihed permissions settings[read & execute/read])

img place holder( of osTicket login screen)
Confirm everything is working by loggining in with creadentials created during osTicket basic installation.
