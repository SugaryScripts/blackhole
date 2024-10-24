```
clone on /home/user/domains/your-domain/your-project
create shortcut your-project/public public-html
change php version on dashboard
use php with
/opt/cloudlinux/alt-php82/root/usr/bin/php

install composer if absolete
cd to your-project


php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === 'dac665fdc30fdd8ec78b38b9800061b4150413ff2e3b6f88543c636f7cd84f6db9189d43a81e5503cda447da73c7e5b6') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

/opt/cloudlinux/alt-php82/root/usr/bin/php composer.phar install
/opt/cloudlinux/alt-php82/root/usr/bin/php artisan key:generate
artisan storage:link
cp .copy.env .env

create database
copy your database into .env

artisan migrate

setup other .env config
done
```

Install composer source
- [Composer](https://getcomposer.org/download/)
- [Custom PHP Version Setup on Hostinger via SSH | by Yauheni Pakala | Medium](https://wcoder.medium.com/custom-php-version-setup-on-hostinger-via-ssh-70289f8fe242)
- [How to Install Composer Locally | Hostinger Help Center](https://support.hostinger.com/en/articles/8727597-how-to-install-composer-locally)

Some troubleshoot composer issue
- [How to Solve Common Composer Issues | Hostinger Help Center](https://support.hostinger.com/en/articles/5792082-how-to-solve-common-composer-issues)
- 