Song CMS  in Symfony.
=====================

A Symfony project created on May 14, 2017, 10:46 am.

Ref: https://github.com/bernardpeh/songbird


…or create a new repository on the command line

echo "# testing" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/pilathraj/songsymfony.git
git push -u origin master
…or push an existing repository from the command line

git remote add origin https://github.com/pilathraj/songsymfony.git
git push -u origin master



CMD:

php symfony new song

$ composer require friendsofsymfony/user-bundle "~2.0"

php bin/console generate:doctrine:entity
php bin/console debug:router | grep fos   for windows uses php bin/console debug:router

# Creating database schema...
php bin/console doctrine:schema:create

#Automated User CRUD Generation
php bin/console doctrine:generate:crud
The Entity shortcut name: AppBundle:User

#clear cache
php bin/console cache:clear
#If no environment is set, the environment is set to develop. To delete prod cache,
php bin/console cache:clear -e prod


#Let us auto-generate the setters and getters for the new $modified and $created variables.
php bin/console doctrine:generate:entities --no-backup AppBundle:User
#The –no-backup option tells the command not to back up your original entity file.

# run this and you will see what the sql is doing
php bin/console doctrine:schema:update --dump-sql
# once you are comfortable with that, force update it
php bin/console doctrine:schema:update --force

# downloaded doctrine fixtures for load data...
$ composer require doctrine/doctrine-fixtures-bundle ^2.3 --dev

# To prove that the install is successful, we should have a new entry in the console php bin/console    --> doctrine:fixtures:load  is available in the list.

mkdir -p src/AppBundle/DataFixtures/ORM

#Now, let us insert the fixtures by running the command line
php bin/console doctrine:fixtures:load -n