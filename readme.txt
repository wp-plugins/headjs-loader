=== HeadJS Loader ===
Contributors: durin
Donate link: http://ilinea.com/
Tags: javascript, js, css
Requires at least: 3.0
Tested up to: 3.1
Stable tag: trunk

A plugin to load your Javascript files via Head JS.  

== Description ==

This plugin reformats your page to utilize <a href="http://headjs.com" title="HeadJS">Head JS</a> in your WordPress site.

It strips out all your old javascript declarations and puts them into head.js calls so that they are loaded in parallel (see the Head JS website for more details).

For example, this:

<pre><code>
<script type='text/javascript' src='http://yoururl.com/wp-includes/js/prototype.js?ver=1.6.1'></script> 
<script type='text/javascript' src='http://ajax.googleapis.com/ajax/libs/jquery/1.4/jquery.min.js?ver=3.0.4'></script> 
<script type='text/javascript' src='http://yoururl.com/wp-includes/js/scriptaculous/wp-scriptaculous.js?ver=1.8.3'></script> 
<script type='text/javascript' src='http://yoururl.com/wp-includes/js/scriptaculous/builder.js?ver=1.8.3'></script> 
<script type='text/javascript' src='http://yoururl.com/wp-includes/js/scriptaculous/effects.js?ver=1.8.3'></script> 
<script type='text/javascript' src='http://yoururl.com/wp-includes/js/scriptaculous/dragdrop.js?ver=1.8.3'></script> 
<script type='text/javascript' src='http://yoururl.com/wp-includes/js/scriptaculous/slider.js?ver=1.8.3'></script> 
<script type='text/javascript' src='http://yoururl.com/wp-includes/js/scriptaculous/controls.js?ver=1.8.3'></script> 
</code></pre>

Becomes:

<pre><code>
<script type="text/javascript" src="http://yoururl.com/wp-content/plugins/headjs-loader/head.min.js"></script> 
<script> 
head.js("http://yoururl.com/wp-includes/js/prototype.js?ver=1.6.1")
    .js("http://ajax.googleapis.com/ajax/libs/jquery/1.4/jquery.min.js?ver=3.0.4")
    .js("http://yoururl.com/wp-includes/js/scriptaculous/wp-scriptaculous.js?ver=1.8.3")
    .js("http://yoururl.com/wp-includes/js/scriptaculous/builder.js?ver=1.8.3")
    .js("http://yoururl.com/wp-includes/js/scriptaculous/effects.js?ver=1.8.3")
    .js("http://yoururl.com/wp-includes/js/scriptaculous/dragdrop.js?ver=1.8.3")
    .js("http://yoururl.com/wp-includes/js/scriptaculous/slider.js?ver=1.8.3")
    .js("http://yoururl.com/wp-includes/js/scriptaculous/controls.js?ver=1.8.3");
</script> 
</code></pre>

If you would like to see Head JS added to the Google CDN library (like I would), then go to <a href="http://code.google.com/p/google-ajax-apis/issues/detail?id=548">http://code.google.com/p/google-ajax-apis/issues/detail?id=548</a> and star the issue.

== Installation ==

1. Upload `headjs-loader` directory to `/wp-content/plugins/` directory
2. Activate the plugin through the 'Plugins' menu in WordPress

== Screenshots ==

== Frequently Asked Questions ==

= No questions =

No answers.

== Upgrade Notice ==

= 0.1.1 =
Fixed bug that caused apache erorr messages if no javascript was declared.

== Changelog ==

= 0.1.1 =
* Fixed bug that caused apache erorr messages if no javascript was declared.

= 0.1 =
* Initial release.
