Applications Management System Library for PHP (AppsCMS) - RELEASE NOTES
========================================================================
see Licence in cms/LICENCE.txt
<!-- SVN Build: $Id: ReleaseNotes.md 2067 2021-04-13 06:11:26Z robert0609 $ -->

![AppsCMS Logo](cms/images/AppsCMS_logo_small.gif)

Released AppsCMS to the public domain under the BSD 3-Clause licence.
See "https://opensource.org/licenses/BSD-3-Clause"

Release Notes - V2.27-1 April 2021
--------------------------------
Minor improvements for contact us plugin.
Improvements to debug tracking comments.

Release Notes - V2.27 April 2021
--------------------------------
Minor improvements

Release Notes - V2.26-9 April 2021
----------------------------------
Bug fix minify cache.
Improved fuse mount option to allow concurrent access to RO ./cms
Turned off load JS with async for AppsCMS library files.
Added AppsCMS version to minified filenames to stop old files being used.
Added cms_rebuild.sh and cms_set_permissions.sh to (DOCROOT) on read only systems
Added php-fpm restart notes.

Release Notes - V2.26-8 April 2021
----------------------------------
Added notes on required system packages for squashfuse.
And improved the install to check server requirements.
And an example of an apache virtual host config,
and an example of an aliassed installation.

Release Notes - V2.26-7 April 2021
----------------------------------
Added enable for AppsCMS drag and drop preload.
And added cms_drag_drop.js to seperate js functions.
Changed ini section "CustomThemeSettings" to "CustomThemeSettings"
Bugfix

Release Notes - V2.26-6 April 2021
-------------------------------------
Removed obsolete admin CSS settings.
Fixed nav bar drop under bug.
AppsCMS now available in a read only library (see installation instructions).
Added quill WYSIWYG.
Improvements to WYSIWYG ops.
Simplified the installer scripts.
Many other improvements.

Release Notes - V2.26-5 February 2021
-------------------------------------
Bugfixes and Improvements

Release Notes - V2.26-4 February 2021
-------------------------------------
Improvements.

Release Notes - V2.26-3 February 2021
-------------------------------------
Bugfixes and improvements.

Release Notes - V2.26-2 February 2021
-------------------------------------
Fixed local sudo checks.
Locale bugfix.
Apache 2.2 (and less) support removed
Bugs with small app admin fixed.

Release Notes - V2.26-1 January 2021
-------------------------------------
Clean up for removed cms_error.php file.
added cms/docroot_files/ directory to provide a copy the current AppCMS docroot files.

Release Notes - V2.26 January 2021
-------------------------------------
Released

Release Notes - V2.25-2 January 2021
-------------------------------------
Upgraded to PHP 7.4
PHP version incompatibility from 7.2 to 7.4 in the global_error_handler().
Revised file headers.
Fixed colour contrast bug in coloured drop downs.
Not released.

Release Notes - V2.25-1 December 2020
-------------------------------------
Bugfix

Release Notes - V2.25 December 2020
-------------------------------------
Added user user stats admin page.

Release Notes - V2.24-2 December 2020
-------------------------------------
Added H1 and H1 title to body/app page configs.
Bugfix

Release Notes - V2.24-1 November 2020
-------------------------------------
Bugfix

Release Notes - V2.24 November 2020
-----------------------------------
Released.

Release Notes - V2.23-RC5 November 2020
--------------------------------------
Bugfixes and improvements.

Release Notes - V2.23-RC4 November 2020
--------------------------------------
Bugfixes and improvements.

Release Notes - V2.23-RC3 November 2020
--------------------------------------
Improvements to the reverse proxy.
Removed the <IfModule mod_rewrite.c> requirement fom the .htaccess
Disengaged_htaccess() check.

Release Notes - V2.23-RC2 November 2020
--------------------------------------
Improvements to the reverse proxy.
Improvements and bufixes MySQL DB ops.

Release Notes - V2.23-RC1 November 2020
--------------------------------------
Added improvements to the way that bookmark imports work.
Added DOCTYPE NETSCAPE-Bookmark-file-1 importer.
Added inline images and icon storage.
Added detector for Google Bot mobility test to trigger tiny version.
Added username http logging.
Added user stats report page.
Added reverse proxy.
Added Proxy Framed Applications.
Improvements and bugfixes.

Release Notes - V2.22-5 September 2020
--------------------------------------
Fixed bug in link editor.

Release Notes - V2.22-4 September 2020
--------------------------------------
Import table from CSV bugfix.
Fixed bug in WS closed operation.

Release Notes - V2.22-3 August 2020
-----------------------------------
Improvements to background multi-download and browser caching.
Improvements for Google Chrome.
Typographic corrections.

Release Notes - V2.22-2 August 2020
-----------------------------------
Added CLI cms/cli/cms_updateAppsCMS.sh shell script.
Improvements to rebuild.

Release Notes - V2.22-1 August 2020
-----------------------------------
Removed cms_user_inline_html preference (now follows the global setting) per user requests.
iframe bugfix

Release Notes - V2.22 August 2020
---------------------------------
Milestone release.

Release Notes - V2.21 August 2020
---------------------------------
V2.21 not released.

Release Notes - V2.21-RC8 August 2020
-------------------------------------
Improvements to EULA operation.
Improvements for preloaded JS, CSS and background images.
Improvements in cache control.

Release Notes - V2.21-RC7 August 2020
-------------------------------------
Removed <cms_page_body_elem>, <div id="cms_page_body_base_overlay"> and <div id="cms_page_base">,
and the associated JS code per programmers requests.
Untangled the page_container and removed the page_container table.
Fixed table captions and removed conditional output.
Improvements
Bugfixes

Release Notes - V2.21-RC6 July 2020
-----------------------------------
Improvements
Bugfixes

Release Notes - V2.21-RC5 July 2020
-----------------------------------
Added number input with min/max for DB configs
Improvements to bookmark imports.
Bugfixes

Release Notes - V2.21-RC4 July 2020
-----------------------------------
Improvements to changing section and link values.
Bugfixes

Release Notes - V2.21-RC3 July 2020
-----------------------------------
Added admin comments column to AppCMS config tables.
Improvements to global error handling.

Release Notes - V2.21-RC2 June 2020
-----------------------------------
AppCMS now uses URI name "cms_action" instead on "action" (leaving "action" available to applications).
Bugfixes

Release Notes - V2.21-RC1 June 2020
-----------------------------------
Added AppsCMS updater (checks if update is available, the update is still done manually).

Release Notes - V2.20-3 June 2020
---------------------------------
Improvements to theme generator.
(Not generally released)

Release Notes - V2.20-2 June 2020
---------------------------------
Added system package dependencies for locale and locality.
Put missing ldap, geoip, Ziparchive, locale_accept_from_http and posix functions as warnings
	when checking installs.

Added open all links in section tabs.
The JS initialize body functions can now be overridden;
+	cms_drag_start(event) looks for app_ov_drag_start(event),
+	cms_drop(event) looks for app_ov_drag(event),
+	cms_drag_over(event) looks for app_ov_drag_over(event).

Added admin edit filters to links, sections, users and groups.
Moved CMS_USER_TIMEOUT_SECS and CMS_USER_COOKIE_TIMEOUT_SECS to
cms.ini, [SessionSettings] section;
SESSIONS_USER_TIMEOUT_SECS and SESSIONS_COOKIE_TIMEOUT_SECS
to stop duplication of session timeout requirement.
Fixed Google mobility issue.
Fixed the ajax base ref protocol bug.
Fixed missing admin search results.
Added clone options.
Added feeble password strength check as per many requests.
Added CMS_WS_DIR to use instead of CMS_DIR to match other defines per many requests.
Bugfixes and improvements.

Release Notes - V2.20-1 May 2020
--------------------------------
Renamed class Ccms_box_tool_tips to Ccms_drop_box and rename the block() method to hover_block() and add panel_block() method
Added show error (etc.) message when logged in.
Added Ccms_sm::get_or_post_app_session() method to better use session saved variables for each app.
Fixed the bugs in CSS and JS minify and the min cache and added src file change detection.
Fixed password reveal or show.
Fixed MySQL table editor prev and next page navigation.
Put code back to PHP 5 compatibility.
Bugfixes and improvements.

Release Notes - V2.20 April 2020
--------------------------------
Finally changed the URI action key variable and URI ajax key variables for the AppsCMS
  to be prefixed by cms_ as many have requested allowing apps to perform similar actions.
Fixed missing settings keys and value, to use default values.
Added cms/cms_init.php for quicker and easy low end integration.
Bugfixes and improvements.

V2.20 Stats
==================================================
|Source         |Lines     |Words     |Bytes     |
|---------------|---------:|---------:|---------:|
|cms/(php)      |     57301|    230176|   2140710|
|cms/(js)       |      2198|      8323|     71789|
|cms/(css)      |       103|       283|      2262|
|cms/(sh)       |      1400|      4544|     32491|
|cms/(html)     |       146|       675|      5589|
|cms/(htm)      |         0|         0|         0|
==================================================

Release Notes - V2.19-13 April 2020
-----------------------------------
Changed the grid input control type 'input' for grid_input_form_elems() to 'multi_input' to avoid confusion standard html element types.
Added /etc/ssl directory.
Added asterisk (* = any key) key to DottedKeys base methods.
Changed get_cms_ini_value($sect_name, $key) to get_cms_ini_value($key, $sect_name = false)
Added get_apps_ini_value($key,$sect_name = false) as apps counterpart to get_cms_ini_value($key, $sect_name = false)
Changed the drop box menu filter to 12 entries minimum.
Sanitized the layout configuration.
Added option browscap client detectors.
Bugfixes and improvements.

Release Notes - V2.19-12 March 2020
-------------------------------------
Umask hot fix.
Added extension interface for app settings.
Typographic fixes to technical manual.
Many requested small improvements added.

Release Notes - V2.19-11 March 2020
-------------------------------------
Performance improvements.
Updated cms/lib/parsedown-1.8.0 (+ modified blockComment() to work with comments like github)

Release Notes - V2.19-10 February 2020
-------------------------------------
Improvements to session handling.

Release Notes - V2.19-9 February 2020
-------------------------------------
Made the cms.sqlite.json rebuild a CLI option.
Improvements in reconstruction.
User session browsing added for some session types.
Added <tr> hover hi-lite option.

Release Notes - V2.19-8 February 2020
-------------------------------------
Hot fix bug fixes

Release Notes - V2.19-7 February 2020
-------------------------------------
Improvements and bug fixes to links operation and DB reconsruction.

Release Notes - V2.19-6 February 2020
-------------------------------------
Improvements to DB code separation for AppsCMS specific classes and general classes.
Added workarounds for incompatible SQLite3 versions (encrypted or not) between operating systems.
Clean up rebuild/repair code.

Release Notes - V2.19-5 February 2020
-------------------------------------
Improvements AJAX JSON POST data.
Added automatic alternatives to 'application/json' and 'application/x-www-form-urlencoded' for POST data
Added do_app_warnings() (e.g. "Cexample_app::do_app_warnings()") for apps to test the installation when the administrator ogs in.
Corrections to manual.

Release Notes - V2.19-4 February 2020
-------------------------------------
Corrected charset anomaly for "&trade;" (0xe2) symbol.
Corrected to LICENSE.txt file to English LICENCE.txt
Added client metadata ajax call to save in session.

Release Notes - V2.19-3 February 2020
-------------------------------------
Hot fix for PHP 5 and orphan settings removal.

Release Notes - V2.19-2 February 2020
-------------------------------------
Bugfixes

Release Notes - V2.19-1 February 2020
-------------------------------------
Added orphaned settings removal when running the CLI rebuild.
Fixed rebuild bugs cause when upgrading from old versions.
General bug fixes and improvements.

Release Notes - V2.19 January 2020
-------------------------------------
Added example application openstreets Where Am I package.
Renamed save_ini_settings() and save_ini_settings() methods in cms and apps to stop inheritance problems.
Improvements to section/section operation.
Updated iframe checking
Added phone number login (along with username and email address).
Added the Ccms_sm and Ccms_base_sm (state machine) classes for improved operation on mobile devices and tablets.

Release Notes - V2.18-2 January 2020
-------------------------------------
Added Version to output on install script.
Improvements to Links_Manager import.
Added links to sitemap.
Rationalized sitemap settings.
Added OpenstreetsMaps Openlayers library.
Bugfixes and typos
Never released.

Release Notes - V2.18-1 January 2020
-------------------------------------
PHP 5.3 compatibility issuse.
Removed set_permisions by default from cms_rebuild.sh

Release Notes - V2.18 December 2019
-------------------------------------
Added option INI_ANALYTICS_EXT_INHEAD_BOOL to control the output of the analytics code.
Added section block folding and hierarchical sections to links page.
Added bookmarks (Firefox and Chrome) import.
Added right column facility.
Added ajax call to save user cookie banner close time.
Added client meta data cookie to get client/windows dimensions.
Changed DB (for drop box) to PDB (panel drop box) to avoid confusion with DB for database.
Added keyword filter on PDB menu panels.
Performance improvements.
Bugfixes and user improvements.

Release Notes - V2.17-6 December 2019
-------------------------------------
Bugfixes

Release Notes - V2.17-5 December 2019
-------------------------------------
Added cookie banner.
Changed define key to INI_ANALYTICS_INC to ANALYTICS_EXT_INC to stop conflict with app files
Improvements.


Release Notes - V2.17-4 November 2019
-------------------------------------
Added ALLOW_NON_SSL_LOGIN_BOOL as a work around for Google Chromes (and others) that block certs on local networks/intranets

Release Notes - V2.17-3 November 2019
-------------------------------------
Added a "login required" option to application pages and local tools.
Variable name improvements.
Bugfixes

Release Notes - V2.17-2 November 2019
-------------------------------------
Bugfixes.

Release Notes - V2.17-1 October 2019
------------------------------------
Bugfixes.

Release Notes - V2.17 October 2019
----------------------------------
Minor improvements only.
Released to the master branch.

Release Notes - V2.16 July 2019 (not released V2.16)
----------------------------------------------------
Added INI_SESSIONS_DATA_TIMEOUT_DAYS to help keep disk usage lower
Renamed JS Ccursor class to Ccms_cursor class to stop name conflicts.
Other improvements
Release candidate V2.16rc1

Added doxygen debug links.
Added cron job control.
Added similar, Levenshtein and phonetic search options.
Added alternate odd/even row background colours for links page.
Changed the default way messages are displayed to a closeable stack.
Moved $page_info['login_allowed'] variable to Ccms_auth::is_login_allowed() function to remove duplication.
Fixed the missing login link after session cookie expires.
Release candidate V2.16rc2

Fixed the page_config icon hover enlarge problems.
Added Ccms_app_install class for application packaging (install and update to come).
Bugfix in export.
Updated language and character set selections and usage.
Release candidate V2.16rc3

Added Ccms_app_install class for application packaging, install and update.
Added "Exact" checkbox to search.
Added cms_body_version, cms_body_purpose, cms_body_info1 and cms_body_info2 columns.
	 to bodies table for general usage (keep packaged information in with application).
Bugfix in config.
Release candidate V2.16rc4

Added nav bar links to app installer.
Added Ccms_tool_install class for local tool packaging, install and update.
Release candidate V2.16rc5

Bugfixes
Added "EULA URI Includes Form" to cms_configs table setting.
Improvements.
Release candidate V2.16rc6

Bugfixes and improvements.
Per many requests, fixed the spelling for licence in Australian code
Fixed clean up from package installs.
Added sanity checks to application and local tool, packagers and installers.
Release candidate V2.16rc7

Bugfixes and improvements.
Fixed clean up from package installs.
Added sanity checks to application and local tool, packagers and installers.
Release candidate V2.16rc8

Minor cleanups in theme and grammar/spelling.
Added warning to setting app page to login.
Fixed the CSS class msg_warning now cms_msg_warning
Added a simple themeable JS class Cpopup for alert() and checkbox confirm().
Release candidate V2.16rc9

Improvements and bugfixes
Release candidate V2.16rc10

Bugfix
Tweaks to iframe in page to stop unnecessary scroll bars.
Release candidate V2.16rc11

Bugfix and Improvements
Added no-print to left column and parts of the standard header.
Remove social media plugin Google+
Changed symbolic links to files on install package and zip file (to allow direct download on GitHub)
Added LDAP_SERVER_TIMEOUT setting for variable timeout.
Added DB export and import.
Release candidate V2.16rc12

Improvements to cms_DB* classes for table export and import.
Added remaining image alternate text.
Added configurable password strength settings.
Release candidate V2.16rc13

Changed login to not check password strength to allow use of existing passwords.
Release candidate V2.16rc14

Minor improvements.
Added application individual app.comments.ini and app.defaults.ini configuration resources
Added application individual app.css and app.js resources
Added Ccms_DB_eidt->format_DB_data_value() method to allow custom value formating.
Added option to Ccms::get_body_uri($body = false), it returns the current body uri.
Changed the AppsCMS Ccms::$cDB to Ccms::$cDBcms to stop conflicts with inherited classes.
Release candidate V2.16rc15

Release Notes - V2.15-3 July 2019
---------------------------------
Improvements:
Removed AJAX DB row / form insert in favor of reload.
Split the DB JS off from cms DB classes to a separate cms/cms_DB_edit.js file
Release candidate V2.15rc1

Release Notes - V2.15-2 July 2019
---------------------------------
Bugfix release.

Release Notes - V2.15-1 July 2019
---------------------------------
Bugfix release.

Release Notes - V2.15 June 2019
-------------------------------
Added the SQLite3 'PRAGMA journal_mode = wal;' for improved concurrency.
Added MySQL database create code for AppsCMS MySQL mode."
Fixed bug in image and icon presentation.
Added link and section icons to config DB.
Finished edit links paged to same as sections layout.
Bugfixes and improvements.
Release candidate V2.15rc1
Improvements to the MySQL initialization methods.
Added CMS_C_ALLOW_APPS_DIR_SHARE to allow apps to share directories.
Added public static $body_defines to Ccms_base class for app helpers.
Improvements to performance.
Release candidate V2.15rc2
Updated the local tools directory settings and made improvements.
Added the legal styling and links to default AppsCMS footer (as a default example).
Improvements to theme generator.
Release candidate V2.15rc3
Bug fixes.
Release candidate V2.15rc4
Added JS Ccms_gife class for dynamic table row additions
Added JS cms_addElem_title2tooltip()
Clean up AppsCMS Admin menus.
WYSIWYG config changed from 'cms.wysiwyg.ini' to 'cms_wysiwyg.json' for more flexibility.
WYSIWYG section has been rewritten to simplify config and usage.
Prefixed cms JS classes with Ccms_ and functions with cms_ to avoid conflict with app JS.
Deleted cms_client_visit_cntr.js (the showClientVisitsCntrCookie() moved to the Ccms_cookie class.
Deleted cms_extra_funcs.js (functions moved to cms_body_func.js)
Deleted cms_security.js (functions no longer required)
Added livesearch AJAXed input type.
Release candidate V2.15rc5
Bugfixes
Release candidate V2.15rc6
Added apps/(APP_DIR)/include/
Added apps/(APP_DIR)/include/app_config.php
Editing the AppsCMS tech manual.
Added app readme configs (like terms, etc. using only files) to make a complete set.
Added app release notes configs (like terms, etc. using only files) to make a complete set.
Added app installer cms_body_installed to cms_bodies table for installed third party apps.
Bugfixes and improvements
Release candidate v2.15rc7
Added the Ccms_base_file and Ccms_base_buffer classes to reduce the size of and functionality of Ccms_base class
Removed "cms_user_eula_time", "cms_user_cookie_time", "cms_user_login_count", "cms_user_last_login" and "cms_user_last_logoff"
	from the "cms_users" tables so that the SQLite DB is more compatible with git and svn revision control and
	moved to the VAR_FS_USERS_DIR.
Improved the ugly appearance of input[type=number] spinners.
Moved the MySQL <-> SQLite defintion converters to the database common class.
Release candidate v2.15rc8
Bugfixes and improvements.
Release candidate V2.15rc9

Release Notes - V2.14 May 2019
------------------------------
Improvements to example code.
Added MySQL extras text to MySQL DB installs
Added static methods available for 'cms_config_show_func', 'cms_config_input_func' and 'cms_config_save_func' in cms_configs.
Added unique application class and plugin autoload for individual applications.
Corrections and additions to the technical manual.
Corrected missed db_ function prefixes for; - sanitize_string(), prepare_input(), prepare_search_keyword(),
Added the "cms_body_type" and "cms_body_dir" columns to the "cms_bodies" table and the default application settings.
Added CSS option to turn header, footer and left column printing on and off.
@TODO Fix the log view for compressed files.
Has a release candidate V2.14rc1
Added the (APP_DIR)cli/ directory to pages / apps setup.
Fixed scaling cropping of background images.
Fixed title toolf tip sizing bug.
Added MySQL database and user account setup functions.
Added on screen all messages for debug.
Has a release candidate V2.14rc2
After feedback from several Wampserver and XAMPP users not having posix_ and other functions available,
	these functions have been wrapped to provide some (used in AppsCMS) alternatives as static functions
	in the Ccms_posix class.
Improvements to SQLite3 error handling and startup error handling.
Has a release candidate V2.14rc3
Improvements to OS detection and usage.
Corrections to technical manual.
Has a release candidate V2.14rc4
Added Apache 2.4 version sections to .htaccess files
App directory lib/ added.
Fixed bug in Ccms_posix.
Has a release candidate V2.14rc5
After several requests the library long name has changed from
	"Applications Management System for PHP" to "Applications Management System Library for PHP"
Has a release candidate V2.14rc6
Ccms_install class renamed Ccms_DB_install to align with the DB class naming.
Added Ccms_DB_edit class.
Merge problems fixed from rc6 in Ccms_base and Ccms_html.
Fixes filter select operation to remember previous selections.
Removed the "$db_name_debug" from "Ccms_database_mysql::install_user_privileges_database()" as it was seen as a security problem.
Added the "Ccms_general::do_cms_cli_warnings()"
Added the "Ccms_cli_dialogs_plugin" plugin for CLI ops.
To reduce redundancy "INI_MINIMUM_NAME_LENGTH" replaced by "LMC_MIN_NAME_LEN".
Bugfixes and improvements.
Has a release candidate V2.14rc7
Split Ccms_DB_edit class into Ccms_DB_checks and Ccms_DB_edit classes.

Release Notes - V2.13 May 2019
------------------------------
Bugfixes to default to links set as home page.
Adds Link Manager tools to import process.

Release Notes - V2.12 May 2019
------------------------------
Improvements to MySQL (the NL, ERROR_DECOR_ON, ERROR_DECOR_OFF defines removed).
Bugfixes to MySQL classes.
Fix shell installer.

Release Notes - V2.11 May 2019
------------------------------
Changed ContactusUs::EMAIL_SUBJECT to a multi input.
Changed 'MODAL_HEIGHT' to 'HEIGHT_MODAL' and 'MODAL_WIDTH' to 'WIDTH_MODAL' to stop limitations auto-generated selectors.
Added all HTML5 elements to cms_title_tooltips.js
Removed the "db_" prefix from database methods to conform to general standards for;-
db_query,db_perform,db_input,db_fetch_array,db_get_name,db_free_result,db_connect,db_close,
db_output,db_error,db_num_rows,db_query_unbuffered,db_fetch_array_unbuffered,db_data_seek,
db_insert_id,db_fetch_fields,
Added cms/cli/cms_update_appsV211.sh to update app code.


Release Notes - V2.10 April 2019
--------------------------------
Added Links Manager functionality to AppCMS.
Added Links_Manager basic data import script.
Fixed the scroll to anchor (Top) bugs.
Added login count, last login and last logoff for local authentications.
Added a wider range of incremental setting values for theme .
Bug fixes and improvements

Release Notes - V2.09 March 2019
--------------------------------
Fixed bug in NAV BAR login logout.
Fixed problems with early version dir checks.
Fixed CSS problems in social media plugin descriptions.
Fixed bugs in update sh script for;-
	"login.php" should be "cms_login.php",
	"Capps_auth" should be "Ccms_apps_auth"
Removed 'ON CONFLICT FAIL' in DB cms_users.cms_user_password_md5.
Has a beta release V2.09rc1.
Bug fixes and improvements.
Has a beta release V2.09rc2.
Bug fixes and improvements.
Has a beta release V2.09rc3.
Bug fixes and improvements.
Has a beta release V2.09rc4.
Improvements to polymorphism allowing AppsCMS class to be more useful.
V2.09 never released



Release Notes - V2.08 February 2019
-----------------------------------
A clean up release for the many V2.07  beta releases.

Release Notes - V2.07 February 2019
-----------------------------------
Fixed bug in javascript function names for multi entry settings.
Improvements in multiple input selection code.
Has a beta release V2.07b1.

Fixed bug in data_sep checks.
Has a beta release V2.07b2.

Added vw settings to attribute sizes.
Added login page selection column to page_bodies DB table.
Bugfixes in DB exports.
Added setting option to include apps/stylesheets/apps.css on all body pages in the <head> section.
Moved the standard APPS_ defined to configure.php.
Improvements to return to search operation.
Has a beta release V2.07b3.

Added missing _DIR suffix to directory constants to stop coding confusion on;
	APPS_FS_LIB, APPS_WS_LIB, APPS_FS_IMAGES, APPS_WS_IMAGES, APPS_FS_JAVASCRIPT,
	APPS_WS_JAVASCRIPT, APPS_FS_STYLESHEETS, APPS_WS_STYLESHEETS.
Bugfix in get_header_admin_tools_db_text() to stop doubling up on Admin menu.
Has a beta release V2.07b4.

Added a custom <cms_page_body_elem> which encloses the page body (not the <body> element) that does not include the header, left column nor footer.
Added a <div id="cms_page_overlay"> and <div id="cms_page_base"> for overlays to reference in non full view pages.
Added Cpage_body javascript class.
Improvements to the technical manual.
Added the CMS_C_ALLOW_TEXT_EDITORS config.
Improvements to Cgotcha_plugin.
Improvements to tech manual.
Added the Ccms_modal class.
Has a beta release V2.07b5.

As requested by many developers;
	Renamed AppsCMS files that begin with app_ or apps_ (in the cms/ directory) to cms_ to stop confusion and allow
		better separation with apps/ files
		and move cms/*styles.css files (contains user theme) to the etc/css/ (ETC_WS_CSS_DIR) directory and
		prefix with "cms_" so that everything in the cms/ directory is just for the AppsCMS,
		moved the cms/calendar.js and calendar.css to cms/lib/calendar/,
		this process has been automated by the "cms/cli/update_appsV207.sh" bash script.
Added "cms_" prefix to AppsCMS CSS classes;-
	cms_box_outer_tip, cms_box_inner_tip, cms_msg_*, cms_title_tooltip, cms_nav_bar, cms_page_sitemap
Fixed the duplicating apps login requests.
Has a beta release V2.07b6

Added optional include file URI in WEBSITE_CLOSED_REASON.
Added auto refresh to web site closed screen every 10 minutes.
Added a page/app cms_body_description column to the cms_bodies table.
Added search filter to image list drop downs.
Set the CSS page_config font size to 10px permanently to stop bad theme settings being unrecoverable.
Has a beta release V2.07b7

Fixed bug in Ccms_auth::after_login() method for stand alone logins.
Fixed spelling typo for contactus
Added custom feedback option text to JS class CajaxOps as per user requests
Added Ccms::get_navbar_grid_sanitised() with privileges control per user requests.
Added more theme height options per user requests.
Bugfixes and Improvements.
Has a beta release V2.07b8

Bugfixes and improvements.
Has a beta release V2.07b9

Check PHP version on minify plugin ops.
Bugfixes and improvements.
Fixed the "extra dot" in the timing logs.
Has a beta release V2.07b10

Added LOG_AJAX_DEBUG_BOOL to log ajax requests and responses in debug mode.
Fixed the PHP 5 array_filter() bug with a work around (don't like).

Not released as V2.07

Next Release Notes - V2.06 - December 2018
------------------------------------------
Performance optimization in Cdatabase_sqlite.
Improvements to install processes in Ccms_install and Ccms_general classes.
Added 'no_body' index for to get_admin_uris() methods for app admin extensions.
Added zip log files and limit number of log files options for AppsCMS logs in /var/logs/.
Speed improvements in global definitions.
Fixed the no session cookie bug.
Added Cookies section to AppsCMS manual.
Added cookie policy configurations.
Has an interim release V2.06r1.

Added options for DB query logging to cms_configs table.
Improvements to contactus plugin.
Added more configuration for messages.
Bugfix for value name in configuration editor.
Has an interim release V2.06r2.

Added options filter on select drop downs with improvements to filter operation.
Bugfixes to message output.
Added LOGIN_FAIL2REFERER_BOOL setting.
Bugfix left column position.
Has an interim release V2.06r3.

Added config code to work with symlinked pages/apps.
Bug fix for admin search.
Has an interim release V2.06r4.

Fixed export of apps cms_bodies table.
Added debug msg type.
Added head default extras for meta name and content values.
Added the aliased timezones to timezone selection.
Converted the remaining "\n" strings to PHP_EOL.
Has an interim release V2.06r5.

Bugfix in <head> generator.
Fixed the download link to github.
Fixed https://github.com/AppsCMS/AppsCMS_Latest/blob/master/AppsCMS-Installer-latest.sh to tech manual.
Fixed urls in CSS minified files.
Improvements to multi-line entries settings (e.g. custom colours).
Has an interim release V2.06r6.

Bug fixes to serialization of configuration strings and arrays.
Not released as V2.06

Release Notes - V2.05 - November 2018
------------------------------------
Bugfixes and PHP 5 to PHP 7 compatibility changes.
Added Ccms_apps_base::recurse_copy()
Improvements in browser detection.
Bugfixes and improvements in Cmsgs, Ccms_apps_base and Ccms_edit classes.
Added config DB exports to tables on entry to edit pages.
Added cms/examples/apps/lib/ directory.

Release Notes - V2.04 - October 2018
------------------------------------
Changed the installer script name from "AppsCMS-Vn.nn.sh" to "AppsCMS-Vn.nn-Installer.sh"
Now does not change .htaccess index.php login.php logout.php files when updating.
Bug fix in define REBUILD_MODE.
Added the cms/lib/ directory for 3rd party libraries.
Revised system installed WYSIWYGs.
Added domain SSL checks.
Added the "Cmedia_conv_plugin" class for text and markdown files.
Fixed naming convention on "LOGIN_VIA_HOMEPAGE" to "LOGIN_VIA_HOMEPAGE_BOOL".
Added the validate_email() method for user and domain checks.
Changed contact us messages to appear under the input field.
Fixed the theme colour selector.
Added the required message to Cmsgs class.
Fixed the Contactus cancel button.
Fixed message cnt bug in Cmsgs class,
Added "Cminify_plugin" class for cached CSS and JS minified output.

Release Notes - V2.03 - October 2018
------------------------------------
Changed CMS_DEFAULT_ABOUT_PAGE to INI_DEFAULT_ABOUT_PAGE_BOOL,
Improved login security,
Long name change from "Applications Management System Library for PHP"
	to "Applications Management System Library for PHP".
Improvements to on screen message handling,
Added AppsCMS logo to About AppsCMS page and AppsCMS Manual page,
Added an automated install process.
Many small improvements and bug fixes.

Release Notes - V2.02 - October 2018
------------------------------------
Correct a error in ETC_WS_IMAGES_DIR definition.
Corrections/additions to about and manual pages.
Added on installation to shown the about page.

Release Notes - V2.01 - October 2018
------------------------------------
Initial V2 release.

Release Notes - V2.00 - October 2018
------------------------------------
Web Site: http://www.appscms.org/
GitHub: https://github.com/AppsCMS/AppsCMS_Latest.git

Previously released as BW-CMS V0 and V1 by BRAEWORKS.
AppsCMS is a replacement for BW-CMS.

.EOF.
