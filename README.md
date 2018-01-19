# Passphrase Generator for Wordpress with Bcrypt encryption

A passphrase style password generator for Wordpress with bcrypt password encryption.

So simple, yet so advanced. Easy to use, totally free!
No premium features or any of that kind of stuff, just true free and open source.

## Requirements

The only requirement is that you are running Apache and PHP 5.5



## Installation

Simple install, just download the zip file from Github and extract it.

FTP a-passphrase.php into your server at wp-content/plugins.

Then login to your dashboard and select installed plugins and find Passphrase Generator with Bcrypt, select activate.

We have submitted this plugin to the Wordpress Plugin repository, it will be available on there as well. We will update once it has been approved.


## Customization

Adjusting the results of the passphrase generator could be sone using a text editor or the wordpress plugin editor.
If you want just words and places you can remove the $num, $numa, $numb, $numc and $char. The $chara provides the space in between the words, places, numbers and characters.

You must always make sure the is a . in between each functions.

Example:

return $words[array_rand($words)] . $chara . $places[array_rand($places)] . $chara . $num . $chara . $char[array_rand($char)]; }

Here's an explanation of the example...

return - retrieves the results

SPACE
$words[array_rand($words)] - gives a random result from the words lists
SPACE
.

SPACE

$chara - adds a space in between the generated passphrase results


SPACE
.

SPACE

And so on...


## Compatibility

This plugin has been tested with a boatload of plugins.

Buudypress, bbpress, Trusona, change wp-login, 
security questions, woocomerce and many more.

If you run in to compatibility issues please let us know at https://github.com/kavanaricklyles/ppg-wp/issues

## Improvements

If you have any ideas on how to improve this plugin, please let us know.

## Donate

https://kavanaricklyles.github.io/ppg-wp/thanks.html

