Applications Management System Library for PHP (AppsCMS) - INSTALLATION NOTES
=============================================================================
see "[Licence](index.php?cms_action=cms_text_view&uri=cms%2FLICENCE.txt)"
<!-- SVN Build: $Id: Installation.md 2411 2021-11-26 00:32:45Z robert0609 $ -->

![AppsCMS Logo](cms/images/AppsCMS_logo_small.gif)

Prerequisites:
==============

*	Linux operationg system (e.g. RedHat/Centos 7, SUSE/openSUSE 15, Ubuntu 18, or higher versions).
*	Apache Web Server 2.4.x installed on LINUX.
*	PHP 7.2 (or higher) with PHP SQLite installed,
*	Applications Management System Library for PHP can be setup as an adjunct to an existing web site, or as a new web site. If a
	new web site, the apache web server configuration needs to be setup for the new web site.
*	An SSL certificate, self signed or registered for SSL/https web site encryption.
*	http (port 80) for default home/links page and https (port 443) for login and user designated pages.
*	Applications Management System Library for PHP is not designed to operate inside a frame or iframe.

Read Only AppsCMS Library:
==========================

The AppsCMS library comes with a read only installation option.
To run the read only option the fuse and squashfuse system packages need to be install to provide the fusermount and squashfuse commands.

The presence of (DOCROOT)/cms/cms_index.php is used as a semaphore to indicate that the AppsCMS library is available as read/write.
 If (DOCROOT)/cms/cms_index.php is not present,
 and if the "fusermount" and "squashfuse" utilities are available,
 the AppsCMS is installed as a read only filesystem using (DOCROOT)/cms_lib_sqsh.sqsh
 is mounted at (DOCROOT)/cms/ directory (using the squashfuse utility) and remains persistent for further web calls.
 This makes the AppsCMS code library in (DOCROOT)/cms/ read only and tamper proof.

The mounting and access to the read only (DOCROOT)/cms/ code directory is done by first access to the AppsCMS via the (DOCROOT)/index.php.
If the (DOCROOT)/index.php is customised (usually the case), the read only library engagement can initiated by
adding "include('cms_lib_sqsh.php');" as the first executed line in (DOCROOT)/index.php. Depending on the web application
it maybe necessary to add the first line executed code to login.php, logout.php and any web accessible php code (e.g. ajax code).
Noting that if the (DOCROOT)/index.php is always called first in a session, this will mount the read only AppsCMS library for all further calls until the web server is restarted.

Additionally, where there is several web sites using AppsCMS, the AppsCMS RPM package can be installed.
This will allow the AppsCMS read only library to be mounted in the web site (DOCROOT) directory from a common library.

Notes:

*	If (DOCROOT)/index.php is present, it is not overwritten by updates and must be manually edited
to engage the read only (DOCROOT)/cms/ directory (as above).
*	If the AppsCMS zip file is used (not the .sh installer) the cms_lib_sqsh.sqsh file is not used,
the cms_lib.sqsh.sh, cms_lib_sqsh.php and cms_lib_sqsh.sqsh files (and engagement code) can be removed.
*	If the AppsCMS was previously using a read/write filesystem (not squashed, indicated by the presence of (DOCROOT)/cms/cms_index.php),
the read only library is not used. If the read only library is required, move (or delete) (DOCROOT)/cms/ directory
and reinstall/update the AppsCMS (using the .sh installer then noting the engagement requirements above).
*	The first web call mounts the read only library in the web server user space and will not be available to (nor seen by) normal users.
 The read only library mount done by the web server can be umounted by restarting the web server.
*	If the CLI scripts in the (DOCROOT)/cms/cli/ directory are required, run the (DOCROOT)/cms_lib_sqsh.sh script to mount the
 (DOCROOT)/cms/ directory with the AppsCMS library as the normal (non web server) user.
 To umount a user mounted read only filesystem run "fusermount -u cms"
*	If AppsCMS read only library is required for debugging, run the (DOCROOT)/cms_lib_sqsh.sh script to mount the
 (DOCROOT)/cms/ directory with the AppsCMS library as the normal user.
 The is will allow the IDE and debugger access to the read only AppsCMS library.
 Otherwise copy the cms directory in the AppsCMS zip file to the (DOCROOT)/cms/ directory (giving read/write access).
*	The user_allow_other is required in /etc/fuse.conf to allow sharing of cms_lib_sqsh.sqsh library mount between command line and web server.
*	The AppsCMS library package is installed in the "/usr/local/share/AppsCMS" directory.

The cms_rebuild.sh and cms_set_permissions.sh scripts in the (DOCROOT) are to make it easier for common command line rebuilds.

Important Note:

The Apache web server will needed to be stopped and started after a read only install or update.
The server will need to be totally disengaged (i.e. a full stop, e.g. service httpd stop).
The normal restart only reloads the web server configuration files and will not release the previous squashfs mounts.
Also, if php-fpm is install, php-fpm needs to be stopped and started to release previous php to bytecode caches.

Installation:
=============

1.	If updating the web site, backup the web site.

2.	Download Applications Management System Library for PHP from
	"https://github.com/AppsCMS/AppsCMS_Latest/blob/master/AppsCMS-Installer-latest.sh"
	to a folder in your web sites directory (typically public_html/).

3.	Execute the following in your web sites directory;-
		chmod u+x "AppsCMS-Installer-latest.sh"	# to allow the installer to run
		./AppsCMS-Installer-latest.sh	# to run the installer

4.	If using the read only library (cms_lib_sqsh.ssqsh) run ./cms_lib_sqsh.sh to mount the read only only files (include apps_fs_sqsqh.sh and bodies_fs_sqsh.sqsh).
	Note the sqsh files are only mounted if there destination directories are empty.
	The /cms_lib_sqsh.sh script will check the destination directories before mounting the sqsh files.

5.	Run "sudo bash -e cms/cli/cms_set_permissions.sh". This will set permissions for shell and web server access.

6.	Run "bash -e ./cms_lib_sqsh.sh -r". This will mount readonly filesystems and build the latest settings, configuration DB and directory structure for this AppsCMS version.

7.	Pointer your browser at	"http://your.web.site/site_alias/index.php" (site_alias/ is part of your server setup, usually empty).
	Note that the AppsCMS will also work in an aliased folder.
	When the Applications Management System Library for PHP is first accessed, will create an empty SQLite database.

8.	When no users are setup, a default admin user is;-
	Username: admin
	Paswword: password
	Recommend that the admin username be disabled after you have setup another, more secure, user (with admin rights).

9.	Recommended VirtualHost server configuration for Applications Management System Library for PHP;-
	* SSLStrictSNIVHostCheck off (on https VirtualHost),
	* AccessFileName .htaccess (on both http and https VirtualHosts)

10.	Suggest checking out the "Config" page first.
	Enter/change the default settings to more appropiate values.
	The "Install" page contains installation settings. When updating, goto "Install" (/index.php?action=edit_install) and save to update new values.
	The "Theme" page contains theme values. When updating, goto "Theme" (/index.php?action=edit_theme) and save to update new values.
	The hard coded installation constants are contained in the "includes/cms_configure.php" file. It is recommended
	that this file is made read only.

11.	After updating a site, it is highly recommended that you login as an administrator, the site version number checking will run the Rebuild Setup functionality automatically (will take upto a 1 minute or 2 to respond while the checking and rebuilding is completed).
	If you need to run the Rebuild Setup manually, run the bash script "cms/cli/cms_rebuild.sh" or goto "http://your.web.site/index.php?cms_action=cms_rebuild_setup" as an administrator.
	CAUTION: The update will use default settings for new features. Take note of the messages (e.g.ERROR, WARNING, and INFO).
	The default settings for new features may need to changed to more appropriate values.

IMPORTANT NOTES:
1. If after an update the web site is non functional, there is a recovery command available to help fix this.
2. On a LINUX host, in a console shell, run "cms/cli/rebuild.sh".
3. If upgrading from Links Manager to AppsCMS, run "cms/cli/cms_import_links_manager.sh" to import Link Manager.

AppsCMS base directory structure short list.

\ ((DOCROOT)/alias)            Web site base directory (maybe (DOCROOT) or a directory / alias under (DOCROOT)).
│
├── ./cms_lib_sqsh.sh          Bash/CLI script to mount read only filesystems (to see options -h|--help).
│
├── apps                       Base directory for web applications (apps code supplied by user).
│
├── apps_fs_sqsh.sqsh          Read only mount of the ./apps directory (optional).
│
├── cms                        Base AppsCMS directory (this directory is overwritten by AppsCMS updates).
│
├── cms_lib_sqsh.sqsh          Read only mount of the ./cms directory (optional).
│
├── etc                        Config base directory (this directory contains the configuration files).
│
├── localtools                 Local tools directory (supplied by user).
│
└── var                        Temporary / transitory data directory (should not need backup).


.EOF.



