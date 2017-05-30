Drupal Review Env
=================

The command line tool to launch cloned Drupal environment for review (code review, test, etc...).

Installation
------------

1. Clone this repository
2. Write `env/config.sh` based on `env/default.config.sh`
3. Create MySQL user  
   `$ drupal-review-env setup-mysql-user | mysql`
4. Configure Apache virtual host like `example/apache/review.drupal.test.conf`

Usage
-----

```
Usage: drupal-review-env <command> [args]

Options:
  -h, --help  Print this help

List existing Drupal sites:
  $ drupal-review-env list

Create new Drupal site of branch:
  $ drupal-review-env create <branch-name>

Update source files and apply to Drupal:
  $ drupal-review-env pull <branch-name|site-id>

Update or create if a site does not exist:
  $ drupal-review-env pull --create <branch-name|site-id>

Delete Drupal site:
  $ drupal-review-env delete <branch-name|site-id> [-f]

Display information of Drupal site:
  $ drupal-review-env info <branch-name|site-id>

Rehash symbolic links of webroot
  $ drupal-review-env rehash

Setup MySQL user:
  $ drupal-review-env setup-mysql-user | mysql

```
