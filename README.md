Song CMS  in Symfony.
=====================

A Symfony project created on May 14, 2017, 10:46 am.

Ref: https://github.com/bernardpeh/songbird
CMD:

$ composer require friendsofsymfony/user-bundle "~2.0"

php bin/console generate:doctrine:entity
php bin/console debug:router | grep fos   for windows uses php bin/console debug:router

# Creating database schema...
php bin/console doctrine:schema:create