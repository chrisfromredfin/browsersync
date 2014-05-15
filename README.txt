INTRODUCTION
============

BrowserSync helps you integrate the BrowserSync Node.js module
(http://browsersync.io/) with your Drupal site by including the JavaScript
snippet at the bottom of the page just before the </body> tag.

Here is an example of the JavaScript snippet required by BrowserSync:

<script src='//127.0.0.1:3001/socket.io/socket.io.js'></script>
<script>var ___socket___ = io.connect('http://127.0.0.1:3001');</script>
<script src='//127.0.0.1:3002/client/browser-sync-client.0.9.1.js'></script>

Please note that this module DOES NOT run BrowserSync for you. You will still
need to run it from the command line.

CONFIGURATION
============

To configure this module you are required to add some configuration variables
to your settings.php file:

// Version of BrowserSync used (eg. 0.9.1). Optional as of BrowserSync 0.7.0.
$conf['browsersync_version'] = '0.9.1';

// Whether the snippet needs be added to non-admin pages.
$conf['browsersync_enabled_for_nonadmin'] = TRUE;

// Whether the snippet needs be added to admin pages.
$conf['browsersync_enabled_for_admin'] = FALSE;

// You might need to tweak this to make sure the snippet is the very last thing
// inside the <body> tag.
$conf['browsersync_snippet_weight'] = 100;

// Host or IP address the BrowserSync socket is running on.
$conf['browsersync_socket_address'] = '10.0.1.2';

// Port the BrowserSync socket is running on.
$conf['browsersync_socket_port'] = '3001';

// Port the BrowserSync client is running on.
$conf['browsersync_client_port'] = '3002';


INSTALLATION
============

 1. Configure the module as per described in the configuration section.
 2. Install the module.
 3. Run BrowserSync from the command line
 4. Happy styling!


DEPENDENCIES
============

This module does not depend on any other module.


MAINTAINERS
===========

 *  jorgegc <http://drupal.org/user/834154>
