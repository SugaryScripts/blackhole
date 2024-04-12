url:: [GitHub - fryctze/lamp-config](https://github.com/fryctze/lamp-config)
up:: [[Linux]]
```sh
sudo pacman -S apache
sudo pacman -S mysql
sudo mysql_install_db --user=mysql --basedir=/usr --datadir=/var/lib/mysql
sudo systemctl start mariadb
sudo mysql_secure_installation
sudo pacman -S php php-fpm php-gd
sudo pacman -S phpmyadmin
```
1. Install apache
2. Install mysql
3. setup mysql
4. install php & php-fpm
5. [[#Enable php extension]] in /etc/php/php.ini 
6. install phpmyadmin
7. [[#Create php-fpm & phpmyadmin conf]] in /etc/httpd/conf/extra
8. [[#Enable module and include config file to httpd.conf]]
9. Extra: [[#Alias]] bash zshrc 
10.  [[#Troubleshoots Warning]]
11. Remove root password? [[Mariadb#Remove root password]]

#### Enable php extension
/etc/php/**php.ini**
```json
bz2
gd
iconv
mysqli
pdo_mysql

date.timezone = Asia/Jakarta
```

#### Create php-fpm & phpmyadmin conf
put these files into /etc/httpd/conf/extra/

php-fpm.conf 
```json
DirectoryIndex index.php index.html
<FilesMatch \.php$>
    SetHandler "proxy:unix:/run/php-fpm/php-fpm.sock|fcgi://localhost/"
</FilesMatch>
```

phpmyadmin.conf
```json
Alias /phpmyadmin "/usr/share/webapps/phpMyAdmin"
<Directory "/usr/share/webapps/phpMyAdmin">
    DirectoryIndex index.php
    AllowOverride All
    Options FollowSymlinks
    Require all granted
</Directory>
```

#### Enable module and include config file to httpd.conf
/etc/httpd/conf/**httpd.conf**
```json
LoadModule unique_id_module modules/mod_unique_id.so
LoadModule proxy_module modules/mod_proxy.so
LoadModule proxy_fcgi_module modules/mod_proxy_fcgi.so

// Add this too
Include conf/extra/php-fpm.conf
Include conf/extra/phpmyadmin.conf
```

#### Alias
.zshrc
```sh
function lamp {

# Check for required arguments (action and service name)
  if [[ -z "$1" ]]; then
    echo "Invalid Usage: service_control (start|stop|restart) <service_name>"
    return 1  # Exit with error code if arguments missing
  fi

  # Validate action argument
  if [[ ! ( "$1" == "start" || "$1" == "stop" || "$1" == "restart" ) ]]; then
    echo "Invalid action: $1. Valid options are (start|stop|restart)."
    return 1
  fi

  # Perform systemctl command based on arguments
  sudo systemctl "$1" php-fpm mysqld httpd && echo "Successfully $1 lamp-services" || echo "Failed to $1 lamp-services"
}
```

#### Troubleshoots Warning
##### Solving Warning - cfg is not accessible
`The $cfg['TempDir'] (/usr/share/webapps/phpMyAdmin/tmp/) is not accessible. phpMyAdmin is not able to cache templates and will be slow because of this.`

**Solved by**:
adding this to `/usr/share/webapps/phpMyAdmin/config.inc.php`
or the source `/etc/webapps/phpmyadmin/config.inc.php`
```json
$cfg['TempDir'] = '/tmp/phpmyadmin';
```


##### Solving Warning - configuration file needs a valid key
**Error Message**:
The configuration file needs a valid key for cookie encryption. A temporary key was automatically generated for you. Please refer to the [documentation](http://localhost/phpmyadmin/doc/html/config.html#cfg_blowfish_secret).

**Solved by**:
blowfish secret 
Go to [phpMyAdmin blowfish secret generator](https://phpsolved.com/phpmyadmin-blowfish-secret-generator/?g=[insert_php]echo%20)
And paste it to `/usr/share/webapps/phpMyAdmin/config.inc.php`

