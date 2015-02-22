###Online Blood Bowl League Manager
Online Blood Bowl League Manager is an online game management system for Game Workshop's board game Blood Bowl.

The authors of this program are

Nicholas Mossor Rathmann
William Leonard
Niels Orsleff Justesen
With special thanks to Pierluigi Masia, Mag Merli, Lars Scharrenberg, Tim Haini, Daniel Straalman, Juergen Unfried, Sune Radich Christensen, Michael Bielec, Grégory Romé, Goiz Ruiz de Gopegui, Ryan Williams and Ian Williams.

Bugs reports and suggestions are welcome. 

###Dependencies
* > MySQL 5.*.*
* > PHP 5.2.0

####Installation
1. Download this repo, either by cloning it or downloading the zip. Use "master" branch for the stable release.
2. Transfer the files to your web server - either via FTP/SFTP or direct download.
3. Put the files in a web accessible folder on your server. On a Unix system this may be /var/www/html/obbml/
4. Run the install script (install.php) from a web browser. **Follow all instructions**. If your site is www.allthethingsbbl.co.uk, the url for install.php will be www.allthethingsbbl.co.uk/obblm/install.php.
5. Delete the install.php from your files.


####Initial Setup
Now that you've installed OBBLM successfully, there are some basic setup steps to do before you can begin use.

1. After running the install.php script, OBBLM has created a user called root with password root. Login using this user.
2. Change the password of the root user in Coach corner → Profile. You may optionally change the name of the root user too.
3. Create the **leagues and divisions** you will be using with OBBLM. This is done under the menu item Admin → Management: Leagues & divisions. Note that you can add more leagues and divisions later, you just need at least one to start off with.
4. Now, OBBLM has two types of settings files you need to edit. The **global settings file**, and the **local settings files**.

--1 The global settings file, settings.php, contains settings that apply across all leagues.

--2 The local settings files, located at localsettings/settings_<LEAGUE ID>.php, are individual league settings. There should exist one for each league.
  
  --* Initially the localsettings/settings_1.php file for the league with ID = 1 is created for you. If you are running multiple leagues copy this file to other leagues IDs (e.g. localsettings/settings_2.php, localsettings/settings_3.php etc.). You can find the IDs of the leagues you have created at the bottom of the page in Admin → Import team.
 
  --* Setting up these settings files should be easy since they are self-documented.
 
  --* Note, be carefull editing the settings_none.php file - it is used by OBBLM when no league settings file for a given league exists in the localsettings directory.

5. OBBLM modules are optionally configured in the separate settings file settings_modules.php. Changing module settings there should be straight forward. Note that you in this file can deactivate modules entirely. You should also note that copying entries from this file into local settings files will produce local module settings for that league.
6. Create the league coaches (users) in Admin → Management: User management

##What's next?
You now have a fully setup and usable installation of OBBLM. Further documentation can be found either [Here](http://nicholasmr.dk/obblmwiki/index.php/Main_Page) or [Here](https://github.com/AppleMaster/obblm/wiki)
