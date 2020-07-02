# lando-drupal9
Using Lando and Drupal 9 with xdebug.

# Composer

    composer create-project drupal/recommended-project moduledev

# Troubleshooting Tips
* Xdebug not working with PHPStorm
** In .lando.yml set xdebug to false, rebuild lando, lando rebuild, then set xdebug back to true and rebuild lando again
