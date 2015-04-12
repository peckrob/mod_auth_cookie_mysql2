# mod_auth_cookie_mysql2

**I am not the original author of this code. I am simply providing this code as a somewhat unsupported upgrade to Apache 2.4. Apache 2.2 users can continue to use the old code.**

This is an Apache 2.4 port of the (apparently discontinued) Apache 2.2 mod auth_cookie_mysql2. The original files can be found for download here: http://home.digithi.de/digithi/dev/mod_auth_cookie_mysq

## Installing

You will need the following prerequisites before you begin: 

* gcc 
* make
* Apache 2.4 and the development files (apache2 and apache2-dev on Ubuntu/Debian)
* MySQL and the development files (mysql and libmysqlclient-dev on Ubuntu/Debian)

Then, just download the code and `make` and `make install`.

## Using

Load it into Apache using the following command:

`LoadModule auth_cookie_mysql2_module /usr/lib/apache2/modules/mod_auth_cookie_mysql2.so`

Note that, in Ubuntu/Debian, the "right" way to do this is to create a file called `auth_cookie_mysql2.load` in the `/etc/apache2/mods-available` directory, then `a2enmod` to load it. Alternatively, you can symlink `auth_cookie_mysql2.load` into `/etc/apache2/mods-enabled` and restart Apache.

Configuration has remained unchanged and can be found at the original address above.

**Please note that this code is completely unsupported by me. I'm simply providing this as an upgrade path for those using this mod to migrate to Apache 2.4. It may have unknown or unresolved bugs (but I haven't found any yet).**
