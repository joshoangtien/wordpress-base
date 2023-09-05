# Installation
Open terminal and execute the following command:
#### 1) Copy file ".env.example" to ".env"
```bash
> cp .env.example .env
```

#### 2) Launch the project with docker
```bash
> docker-compose up -d
```

#### 3) Now open the browser and enter the URL - http://localhost:NGINX_PORT/ (NGINX_PORT - environment). It should show the output of index.php.

#### 4) Now, try to access phpMyAdmin from the Browser using the URL http://localhost:PHPMYADMIN_PORT (PHPMYADMIN_PORT - environment). It should show the phpMyAdmin home page.

# Install WordPress
In this step, we will continue with our previous steps and download and install WordPress.

Now, download the WordPress source from the [Official Website]([https://linktodocumentation](https://wordpress.org/download/))

After downloading the wordpress archive, do the extraction in the project "root" folder

Also, copy the *wp-config-sample.php* and paste within the same directory renaming it to *wp-config.php*. 

```bash
> cd root/
> cp wp-config-sample.php wp-config.php
```

Now configure the database as below.

```php
<?php
....
....
define( 'DB_NAME', 'DB_DATABASE environment' );

/** Database username */
define( 'DB_USER', 'DB_USERNAME environment' );

/** Database password */
define( 'DB_PASSWORD', 'DB_PASSWORD environment' );

/** Database hostname */
define( 'DB_HOST', 'mysql' );
....
....
```
