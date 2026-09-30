=== Gallery Sharing ===
Contributors: palasthotel, edwardbock, janaeggebrecht
Donate link: http://palasthotel.de/
Tags: gallery, sharing
Requires at least: 4.0
Tested up to: 4.7.3
Stable tag: 1.0.1
License: GPL-3.0-or-later
License URI: https://www.gnu.org/licenses/gpl-3.0.html

Deprecated and no longer maintained. Please deactivate and delete it.

== Description ==

**This plugin is deprecated and is no longer maintained.** Version 1.0.1 is the
final release: it closes a security issue and adds this notice. Please deactivate
and delete the plugin.

It shared galleries between WordPress installations through a button in the
classic editor. That button never appeared in the block editor, the WordPress
default since 5.0, the sharing relied on fetching rendered HTML across sites, and
the feature is no longer in use. There is no successor.

Adds a new tool to post editor that allows you to share you galleries.

== Installation ==

1. Upload `gallery-sharing-wordpress.zip` to the `/wp-content/plugins/` directory
1. Extract the Plugin to a `gallery-sharing` Folder
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Goto Settings->Gallery Sharing
1. Enter Domain
1. Enter htaccess credentials if needed else leave empty
1. Use tinymce button on post editor to find galleries in all instances and in own wordpress

== Frequently Asked Questions ==

= How does it work? = 
We place a shortcode in post content and register an ajax endpoint. On pageload the shortcode in post content loads via curl the gallery from the registered endpoint and renders it to content.


== Screenshots ==


== Changelog ==

= 1.0.1 =
* Deprecated: final release. The plugin is no longer maintained - please deactivate and delete it.
* Security: the gallery API endpoint no longer exposes draft, pending or private galleries to unauthenticated requests.

= 1.0 =
* First release

== Upgrade Notice ==


== Arbitrary section ==


