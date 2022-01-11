# lando-drupal9
Using Lando and Drupal 9 with Xdebug.

## Versions tested
* Lando: v3.0.5
* Drupal: 9

## Composer
Installing Drupal 9 with composer.

    composer create-project drupal/recommended-project project-name
    
## Drush
Lando no longer installs Drush globally and must include via composer.

    lando composer require drush/drush

## PHPStorm And Xdebug
* Since the port for http can change in Lando, such as when rebuilding Lando, using https for Xdebug with PHPStorm makes sense

## Troubleshooting Tips

### Xdebug not working with PHPStorm?

* In .lando.yml set xdebug to false, rebuild lando, lando rebuild, then set xdebug back to true and rebuild lando again
    
    Set PHPStorm to break at the first line when debugging

* Try a different Debug Port

    Open PHPStorm Preferences -> Languages & Framework -> PHP -> Debug -> Debug Port: 9002
    
    Then in config/php.ini change the xdebug.remote_port value to match e.g. xdebug.remote_port=9002
