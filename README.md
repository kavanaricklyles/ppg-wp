## Bcrypt Encryption

Replace WP's outdated and insecure MD5-based password hashing with the modern and secure bcrypt.

This plugin requires PHP >= 5.5.0 which introduced the built-in password_hash and password_verify functions.

See Improving WordPress Password Security for more background on this plugin and the password hashing issue.

WordPress still uses an MD5 based password hashing scheme. They are effectively making 25% of websites more insecure because they refuse to bump their minimum PHP requirements. By continuing to allow EOL PHP versions back to 5.2, they can't use newer functions like password_hash.

This is a known problem which WordPress has ignored for over 4 years now. Not only does WordPress set the insecure default of MD5, they don't do any of the following:

document this issue
provide instructions on how to fix it and make it more secure
notify users on newer PHP versions that they could be more secure
What's wrong with MD5? Really simply: it's too cheap and fast to generate cryptographically secure hashes.

WordPress did at least one good thing: they made wp_check_password and wp_hash_password pluggable functions. This means we can define these functions in a plugin and "override" the default ones.

This plugin plugs in 3 functions:

wp_check_password
wp_hash_password
wp_set_password
wp_hash_password

This function is the simplest. This plugin simply calls password_hash instead of WP's default password hasher. The wp_hash_password_options filter is available to set the options that password_hash can accept.

wp_check_password

At its core, this function just calls password_verify instead of the default. However, it also checks if a user's password was previously hashed with the old MD5-based hasher and re-hashes it with bcrypt. This means you can still install this plugin on an existing site and everything will work seamlessly.

The check_password filter is available just like the default WP function.

wp_set_password

This function is included here verbatim but with the addition of returning the hash. The default WP function does not return anything which means you end up hashing it twice for no reason.




## Passphrase Generator for Wordpress with Bcrypt encryption

A passphrase style password generator for Wordpress with bcrypt password encryption.

So simple, yet so advanced. Easy to use, totally free!
No premium features or any of that kind of stuff, just true free and open source.

## Requirements

PHP >= 5.5## Bcrypt Encryption

Replace WP's outdated and insecure MD5-based password hashing with the modern and secure bcrypt.

This plugin requires PHP >= 5.5.0 which introduced the built-in password_hash and password_verify functions.

See Improving WordPress Password Security for more background on this plugin and the password hashing issue.

WordPress still uses an MD5 based password hashing scheme. They are effectively making 25% of websites more insecure because they refuse to bump their minimum PHP requirements. By continuing to allow EOL PHP versions back to 5.2, they can't use newer functions like password_hash.

This is a known problem which WordPress has ignored for over 4 years now. Not only does WordPress set the insecure default of MD5, they don't do any of the following:

document this issue
provide instructions on how to fix it and make it more secure
notify users on newer PHP versions that they could be more secure
What's wrong with MD5? Really simply: it's too cheap and fast to generate cryptographically secure hashes.

WordPress did at least one good thing: they made wp_check_password and wp_hash_password pluggable functions. This means we can define these functions in a plugin and "override" the default ones.

This plugin plugs in 3 functions:

wp_check_password
wp_hash_password
wp_set_password
wp_hash_password

This function is the simplest. This plugin simply calls password_hash instead of WP's default password hasher. The wp_hash_password_options filter is available to set the options that password_hash can accept.

wp_check_password

At its core, this function just calls password_verify instead of the default. However, it also checks if a user's password was previously hashed with the old MD5-based hasher and re-hashes it with bcrypt. This means you can still install this plugin on an existing site and everything will work seamlessly.

The check_password filter is available just like the default WP function.

wp_set_password

This function is included here verbatim but with the addition of returning the hash. The default WP function does not return anything which means you end up hashing it twice for no reason.




## Passphrase Generator for Wordpress with Bcrypt encryption

A passphrase style password generator for Wordpress with bcrypt password encryption.

So simple, yet so advanced. Easy to use, totally free!
No premium features or any of that kind of stuff, just true free and open source.

## Requirements

PHP >= 5.5.0
WordPress >= 4.4 (see https://core.trac.wordpress.org/ticket/33904)




## Installation

Simple install, just download the zip file from Github and extract it.

FTP a-passphrase.php into your server at wp-content/plugins.

Then login to your dashboard and select installed plugins and find Passphrase Generator with Bcrypt, select activate.

We have submitted this plugin to the Wordpress Plugin repository, it will be available on there as well. We will update once it has been approved.


## Customization

Adjusting the results of the passphrase generator could be done using a text editor or the wordpress plugin editor.
If you want just words and places you can remove the $num, $numa, $numb, $numc and $char. The $chara provides the space in between the words, places, numbers and characters.

You must always make sure there is a . in between each functions.

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

