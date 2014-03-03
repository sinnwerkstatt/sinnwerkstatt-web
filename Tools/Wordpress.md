# Wordpress

## Strato Installation
define('DB_HOST', 'rdbms.strato.de');    // 99% Chance, dass du hier nichts ändern musst.

If not working:

* Open phpMyAdmin by clicking on Datenbank-Verwaltung
* On right is "Database server" with  ```User: <user-name>@<db-host>```. Try with exaclty this ```<db-host>```
* Then try again with ```rdbms.strato.de```

## Deploy
* Copy files with [* Import the database
    * Change "localhost" to "official_url" (HELP! How to automate this?)
* If using Permalinks, recreate the .htaccess

### Deployed Wordpress Plugins
* [Chap Secure Login](http://wordpress.org/plugins/chap-secure-login/) - Do not show password, during login, on an insecure channel (without SSL). Use a SHA-256 hash algorithm.
* [WP Security](http://wordpress.org/plugins/better-wp-security/) - various security options, makes backups too.
    * Activate backups!!!

## Wordpress Plugins
* [All-in-One Event Calendar](https://wordpress.org/extend/plugins/all-in-one-event-calendar/) - powerful plugin for events.
* [No Self Pings](http://wordpress.org/extend/plugins/no-self-ping/) - remove self pings
* [Contact Form 7](http://wordpress.org/extend/plugins/contact-form-7/) - easy to maintain contact form
* [Efficient Related Posts](http://wordpress.org/extend/plugins/efficient-related-posts/) - shows related posts by tags
* [Enhanced Recent Posts](http://wordpress.org/extend/plugins/enhanced-recent-posts/) - shows recent posts, can exclude posts from categories
* [Like](http://wordpress.org/extend/plugins/like/) - Facebook like button for posts
* [MailChimp Widget](http://wordpress.org/extend/plugins/mailchimp-widget/) - easy and free newsletter by Mailchimp
* [Social Media Widget](http://wordpress.org/extend/plugins/social-media-widget/) - Adds links to all of your social media and sharing site as a widget
* [Solid Code Theme Editor](https://wordpress.org/extend/plugins/solid-code-theme-editor/) - edit ALL theme files
* [W3 Total Cache](http://wordpress.org/extend/plugins/w3-total-cache/) - for caching (performance)
* [XCloner - Backup and Restore](https://wordpress.org/extend/plugins/xcloner-backup-and-restore/) - schedule backups with cron jobs

## Publishing
* [WP to Twitter](https://wordpress.org/plugins/wp-to-twitter/)
* [Facebook Page Publish 2](http://wordpress.org/plugins/facebook-page-publish-2/)

### Security
* [Better WP Security](https://wordpress.org/extend/plugins/better-wp-security/) (deploy) - various options, makes backups too.
    * Warning: don't change the wp-content dir because it may brake the theme and other plugins.
* [Chap Secure Login](https://wordpress.org/extend/plugins/chap-secure-login/) (deploy) - Do not show password, during login, on an insecure channel (without SSL). Use a SHA-256 hash algorithm. (works on v3.5)
* [Really Simple CAPTCHA](http://wordpress.org/extend/plugins/really-simple-captcha/) - needed for Contact Form 7
* [Semisecure Login Reimagined](http://wordpress.org/extend/plugins/semisecure-login-reimagined/) - for more secure login into your Wordpress

### Translate

#### [qTranslate](https://wordpress.org/extend/plugins/qtranslate/)


* Change Blog Title: [* [http://benohead.com/wordpress-qtranslate-clicking-on-the-home-link-resets-to-the-default-language/ Fix Blog Title Link](:en]YourBlogTitle[:de]DeinBlogTitel):
    * open the file qtranslate/qtranslate_hooks.php.
    * Scroll down. At the end of the file, you'll see a bunch of add_filter(...); calls.
    * Add there the following: add_filter('home_url', 'qtrans_convertURL');
* [Make bigger icons](http://www.sewon-akiko.com/wordpress-qtranslate/)
* [Add Language Cookie](http://stackoverflow.com/a/14398434) to save the previous chosen language.

### Navigation
* [Infinite Scroll](https://wordpress.org/plugins/infinite-scroll/)

## Bootstrap CSS
* [Bootstrap](http://twitter.github.com/bootstrap/) - Sleek, intuitive, and powerful front-end framework for faster and easier web development.
* [WordPress Twitter Bootstrap CSS](https://wordpress.org/extend/plugins/wordpress-bootstrap-css/)
* [Extended Walker class for use with the Twitter Bootstrap toolkit Dropdown menus in Wordpress](https://gist.github.com/johnmegahan/1597994)

## Others
* [Add strong tag to the blog description.](http://stackoverflow.com/questions/4502086/is-there-a-way-of-adding-strong-tags-in-wordpresss-description-tagline-area) - change your header file accordingly.
* How to [create shortcodes](http://wp.smashingmagazine.com/2012/05/01/wordpress-shortcodes-complete-guide/) and [nested shortcuts](http://www.sitepoint.com/wordpress-nested-shortcodes/).
