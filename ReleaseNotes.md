Applications Management System Library for PHP (AppsCMS) - RELEASE NOTES
========================================================================
see "[Licence](index.php?cms_action=cms_text_view&uri=cms%2FLICENCE.txt)"
<!-- _SVN_build: $Id: ReleaseNotes.md 2914 2022-10-25 14:32:35Z robert0609 $ -->

![AppsCMS Logo](cms/images/AppsCMS_logo_small.gif)

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
