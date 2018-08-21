# Simple Drupal8

Composer created simple Drupal8 project for testing deployment and management on both PAS and PKS.

## Issues

Drupal8 is typically configured to use data sources in settings.php.  This needs to be modified to get configureation from VCAP (and ultimately CredHub)

Drupal8 dependancies can be vended on deployment, but this takes time and can have issues when internet access is limited.  What is best practice to vend and deply the dependancies?  As part of build pipeline seems a good potential solution.

Drupal8 on initialization creates a bunch of directories/files that are then registered in the DB tables.  This structure needs to be replicated across all nodes, and is hard linked to the DB data.

Drupal8 is designed to be updated in place.

## Project notes

Created with composer:

```
composer create-project drupal-composer/drupal-project:8.x-dev some-dir --stability dev --no-interaction --no-install
```
