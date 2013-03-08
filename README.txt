Drupal Bookmarks with login reminders Module
============================================
http://drupal.org/project/bookmarks2


## Description
A simple bookmarks module with some advanced features like

bookmarks RSS feed per user
sorting bookmarks in folders
optional login/password reminder with encryption
optional column consolidation in the link display page
Please seriously consider SSL encryption for your site, if you want to use the login/password reminder functionality.

Originally branched from bookmarks module [1]
[1] http://drupal.org/project/bookmarks

## Requirements
Drupal 5.x

## Installation
1. Create the SQL table.
     mysql -u username -ppassword drupal < bookmarks2.sql

2. Copy bookmarks2.module and trash.gif under Drupal's modules/bookmarks2
   directory. Drupal should automatically detect it. Enable the module via
   the administer >> modules page.

3. Enable the 'User Bookmarks' block on the administer >> blocks page.

4. Add "access bookmarks" permission to those roles, who you would like to
   add bookmark support. Note that since bookmarks are stored for users
   only, it is not possible to let anonymous users to have bookmarks.

5. If you have a custom theme, you can customize the delete icon by
   defining a themename_bookmarks2_del() function (replacing 'themename'
   with the name of your theme). See the theme_bookmarks2_del() implementation
   in bookmarks2.module. The bookmarks block is also themeable (via
   theme_bookmarks2_block()).

   Bookmarks related links will appear under the user's own menu. If you need
   to have a 'bookmark this page' link somewhere in your theme, use the
   user/$user->uid/bookmarks2/add/quick URL target for the link (where
   $user->uid is the user identifier).

## Authors
David Kent Norman <deekayen [at] deekayen {dot} net> (maintainer)
Sponsored by Advanced Automation http://www.advancedautomationinc.com/

Marco Molinari <marco [at] porciletto.org>
Al Maw         <drupal [at] almaw.com>
Matt Westgate  <drupal [at] asitis.org>
Gabor Hojtsy   <goba [at] php.net>

## History
This module idea came from kuro5hin, and it was originally created by
Marco Molinari <marco [at] porciletto.org>. Updated Feb 2003 by Al Maw
<drupal [at] almaw.com> to work with Drupal CVS (clean URLs).
Also renamed "bookmarks", as that seemed a great deal more obvious.
The module was mostly rewritten in October 2003 to support arbitrary
Drupal URL bookmarks by Gabor Hojtsy (<goba [at] php.net>). Matt Westgate
rewritten the module to make it capable of handling outbound links in
February 2004. David Kent Norman forked the bookmarks module to
bookmarks2 to add some controversial features and keep a simpler alternative.

## Bug reports and feature requests
1. Go to the module issue queue at http://drupal.org/project/issues/bookmarks2?status=All&categories=All
2. Click on CREATE A NEW ISSUE link.
3. Fill the form.
4. To get a status report on your request go to http://drupal.org/project/issues/user


## UPGRADING
Read more at http://drupal.org/node/250790

## License
Licensed under the GNU General Public License, GPL v2.

