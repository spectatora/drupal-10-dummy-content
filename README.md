
# How to install Drupal 10 and generate dummy content in 10mins


# We have
- xampp
- composer - 2.5.4

# 1. Install Drupal

https://www.drupal.org/docs/develop/using-composer/manage-dependencies

```composer create-project drupal/recommended-project drupal```


# 2. Create a databse in phpmyadmin

```drupal -> utf8mb4_general_ci```

# 3. Alter vhosts file 

```
<VirtualHost *:80>
 DocumentRoot "C:/xampp/htdocs/drupal"
 ServerName my-drupal.com
 <Directory "C:/xampp/htdocs/drupal">
 Options Indexes FollowSymLinks MultiViews
 AllowOverride all
 Order Deny,Allow
 Allow from all
 Require all granted
 </Directory>
</VirtualHost>
```

# 4. Install theme 

https://www.drupal.org/project/tara

```composer require drupal/tara:^10.0```

# 5. Install Drush
https://www.drush.org/11.x/install/


```composer require drush/drush```


# 6. Generate dummy content


```composer require 'drupal/devel:^5.0'```
