# Install & Configure Platform

## Requirements {#requirements}

Platform is essentially just a series of components that work with Laravel. So the requirements are virtually the same. However some components may require dependencies with there own set of minimum requirments.

- PHP >= 5.3.7
- MCrypt PHP Extension


## Download Platform {#download}

You can get Platform by cloning the repository from GitHub.

	git clone git@github.com:cartalyst/platform.git my-project

Platform can also be installed by simply [downloading a copy from GitHub](https://github.com/cartalyst/platform/archive/master.zip). After downloading, unzip the `.zip` file into a location that suits you.

> Installing by cloning from the GitHub repository is the preferred method as this gives you an easy way to update Platform by merging changes from the original GitHub repository.


## Composer {#composer}

After getting Platform, you can install all of Platform's dependencies by running a composer install command in your CLI. Navigate to your Platform folder and run the following command:

	composer install


## Configure Laravel {#configure-laravel}

Before you can get started with Platform, you'll still have to configure the Laravel 4 framework. Platform is built with Laravel 4 so some configuration is necessary. Please follow all steps detailed in [the Laravel 4 configuration documentation](http://laravel.com/docs/installation#configuration).


## Permissions {#permissions}

Platform requires the following folders to have write access by the web server:

- The `app/config` folder (necessary for writing the Platform config files).
- The `app/storage` folder and its sub-folders.
- The `public/cache` folder and its sub-folders.


## Trusted IPs {#trusted-ips}

If you aren't installing on your localhost you can add trusted IP's to the installer's config file in `app\config\packages\platform\installer\config.php`.


## The CLI Installer {#the-cli-installer}

The easiest way to install Platform is to run the CLI installer. Just run the following command and follow all of the steps.

	php artisan platform:install


## The Browser Installer {#browser-installer}

You should see the Platform installer when you navigate to the project in your browser. Follow the on screen instructions.


## Custom Installer {#custom-installer}

You may also choose to use your own installer by extending ours or completely replacing it.

Platform is an application-base, and thus it is flexible.

If you're distributing an app, you probably don't want a Platform installer for it, you probably want your own installer with your own custom logic.

Just change the requirements in `composer.json` and register your own installer's service provider.
