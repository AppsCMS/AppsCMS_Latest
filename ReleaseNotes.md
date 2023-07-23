Applications Management System Library for PHP (AppsCMS) - RELEASE NOTES
========================================================================
see "[Licence](index.php?cms_action=cms_text_view&uri=cms%2FLICENCE.txt)"
<!-- _SVN_build: $Id: ReleaseNotes.md 3386 2023-07-23 09:40:08Z robert0609 $ -->

![AppsCMS Logo](cms/images/AppsCMS_logo_small.gif)

Release Notes - V3.07.5 - July 2023
-----------------------------------
Added JSON array signing.

Release Notes - V3.07.4 - July 2023
-----------------------------------
Improvements and bugfixes to block layout.

Release Notes - V3.07.3 - April 2023
------------------------------------
Updated documents.
Changed from using "fusermout -u" to "umount" to unmount squashfs filesystems.
Bugfixes and improvements.

Release Notes - V3.07.2 - April 2023
------------------------------------
Updated the PHPMailer to 6.8.0
Bugfixes and Improvements

Release Notes - V3.07.1 - April 2023
------------------------------------
Bugfixes and Improvements

Release Notes - V3.07 - March 2023
----------------------------------
Released

Release Notes - V3.06.RC1 - March 2023
--------------------------------------
Changed the version format to be compatible with system package names (e.g. from V3.06-RC1 to V3.07, i.e. no dashes, dashes used for system package release).
Added application sub-applications.
Added LittleShop online shop application example.
Important Changes per many requests;-
	1. Changed javascript/ directories name to js/,
	2. Changed stylesheets/ directories name to css/,
	3. Added a cms/cli/upgraders/cms_upgrade_v305.sh (see --help) to upgrade directories.
Added the (APPS_DIR)/include/apps_head_inc.php and (APP_DIR)/include/app_head_inc.php provision for custom head content.
Added application and tool copyright messages.
Added applications media/ directory for direct browser access to media (images,icons,videos, etc.).
Improvements and bugfixes.
Release candidate

Release Notes - V3.05 - February 2023
-------------------------------------
Added sha256 checksums for distribution files.
Released

Release Notes - V3.04 - February 2023
-------------------------------------
Improvements to RPM build.
Changed AppsCMS*.rpm to AppsCMS-Library*.rpm
Added AppsCMS-Docs rpm (also contains the example code).
Released

Release Notes - V3.03-RC8 - February 2023
-----------------------------------------
Added basic application type.
Fixed bug in cms/cli/cms_set_permissions.sh
Renamed class Ccms_config to Ccms_config_funcs to better reflect use
Added class Ccms_appointments_plugin for appointment scheluding.
Improved legal documents interface.
As per requests;-
	::is_user_logged_in() is now ::is_cms_user()
	::is_admin_user() is now ::is_cms_admin_user()
	::is_apps_user() is now ::is_cms_apps_user()
	::is_api_user() is now ::is_cms_api_user()
	::is_group_manager() is now ::is_cms_group_manager()
	added ::is_cms_app_manager()
	added ::is_cms_guest() for completeness
Added SMS messaging.
Improvement to DB reconstruction from JSON.
Added settings for HTTP and HTTPS ports.
Added email and mobile verification.
Added settings filter function to settings edit classs.
Added body page maximum width settings.
Other improvments and bugfixes.

Release Notes - V3.03-RC7 - October 2022
----------------------------------------
Fixed links filter bug.
Fixed the class interface check bug.
Fixed apps settings for images bug.
Fixed cms/lib class autoload bug.
Changed the etc/ and var/ directories to the apache server user name permission.
Added theme settings for top memus, top title and top authorization sections.
Moved example out of the AppsCMS, now in a dist-pkgs/examples/ directory.
Improvements.

Release Notes - V3.03-RC6 - October 2022
----------------------------------------
Added .scss JIT compiler, dart-sass, and interface code through the Minify plugin for .css generation.
Fixed API IP check bug.

Release Notes - V3.03-RC5 - October 2022
----------------------------------------
Improved the theme and CSS generation.
Websockets SWOOLE server code has been removed in favour of external application dedicated server instance (e.g. swoole or node.js).
Changed LMC_ configuration prefix to LM_C_ for AppsCMS configuration defines to avoid conflicts with application defines.
Changed INI_ settings prefix to CMS_S_ for AppsCMS settings defines to avoid conflicts with application defines.
Bugfixes.

Release Notes - V3.03-RC4 - October 2022
----------------------------------------
Reduced contents cache overhead.
Reduced dynamic minify overhead.
Added Gotcha option to login.

Release Notes - V3.03-RC3 - October 2022
----------------------------------------
Improvements and bugfixes

Release Notes - V3.03-RC2 - October 2022
----------------------------------------
Improved session data security.
Simplified and rewrote the way page layout works and is generated.
Renamed the *.css.php theme generation files.
The variable name app (preferred) and body are now interchangeable in URLs.
Improvements and bugfixes

Release Notes - V3.03-RC1 - August 2022
------------------------------------------
Remove ->logEvent() dynamic method, now using ::log_info_msg() static method
Removed unused composer packages.
Updated cms/lib/translate_shell/
Improvements and bugfixes

Release Notes - V3.02 - August 2022
----------------------------------
Added "cms_"prefix to AppsCMS variables to stop variable name conflict.
Removed Ccms_reverse_proxy class.
Added apps/include/apps_rebuild.php
Added virtual folders access
Added multi-language code
Added class Ccms_language language translation
Improvements and bugfixes

Release Notes - V3.01 - April 2022
----------------------------------
Added Variable to set maximum inline nav bar tool inclusion.

Release Notes - V3.00-RC3 - April 2022
------------------------------------------
Changes to websockets operation (removed tcp, udp and http servers code, leaving only draft websockets code).
Fixed contactus subject encoding.
Added index.php?cms_action=cms_version
Improvements and bugfixes

Release Notes - V3.00-RC2 - January 2022
-----------------------------------------
Improvements and bugfixes

Release Notes - V3.00-RC1 - December 2021
-----------------------------------------
First release of V3.00 as RC1..
Upgrade and replacement for AppsCMS V2.

Moved domain site data to etc/variables/.
Improvements to to site data (i.e. access counter) reliability.

Previously released as AppsCMS V2.

.EOF.
