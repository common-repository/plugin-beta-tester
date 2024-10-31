=== Plugin Beta Tester ===
Tags: beta, advanced, testing, plugins, plugin
Donate link: http://tinyurl.com/donatetomitcho
Contributors: mitchoyoshitaka
Tested up to: 3.8
Requires at least: 3.0
Stable Tag: 0.5

== Description ==
This plugin aids with beta testing WordPress plugins hosted on [wordpress.org](http://wordpress.org/extend/plugins/). Once Plugin Beta Tester is activated, WordPress will notify you of new beta versions of plugins, not just new stable versions, and you'll be able to upgrade to these beta versions with just one click within WordPress.

Make sure to make frequent backups while you beta test plugins, and make sure to report bugs. Thanks for helping test plugins!

== Changelog ==

= 0.5 =
* Updated for WordPress 3.7, which [changed the way plugin update checks happen](http://make.wordpress.org/core/2013/10/25/json-encoding-ssl-api-wordpress-3-7/).

= 0.4 =
* Some plugins would not get checked properly, due to core bug [#15058](https://core.trac.wordpress.org/ticket/15058). Now MD5-ing plugin slugs so they have safe transient names to get around this bug.
* Make the `version_compare` function a bit more robust
* Made more strings localizable

= 0.3 =
* Using [new wordpress.org API for version checks](https://core.trac.wordpress.org/ticket/18477), to be much more performant. Props nacin, sc0ttkclark.
* Added transient, so beta checks only occur once a day. Can be changed using the constant `PLUGIN_BETA_TESTER_EXPIRATION`.
* Added filter `pbt_versions` so other plugins can hook into responses. `pbt_versions` filters an object with the `latest` and `stable` version strings for a particular plugin.

= 0.2 =
* No longer looks for updates on every admin page load
* Assume directory name is plugin slug
* Code cleanup: now object-oriented

= 0.1 =
* Initial upload

== Installation ==

1. Upload to your plugins folder, usually `wp-content/plugins/`
2. Activate the plugin on the plugin screen.
3. Visit Plugins and see if you have any new betas to try out.

== Screenshots ==

1. The upgrade message on the Plugins page clearly marks beta releases.
2. Plugins on the Tools > Upgrade page also are clearly marked as betas.
