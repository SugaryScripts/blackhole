# Command
#### Database
```mysql
CREATE DATABASE my_database;
DROP DATABASE my_database;
USE my_database;
```
#### Table

```mysql
SHOW TABLES FROM my_database
```


# Case
## Login
```sh
mariadb -u fryctze -p
```
- -u : Specify the user u want to connect as
- -p : Tells `mysql` client to prompt for a password. Without it, might not work if the user requires one

## Remove root password
latest_executed:: on ver 11.3.2
source:: [How to remove MySQL root password - Stack Overflow](https://stackoverflow.com/questions/3032054/how-to-remove-mysql-root-password)
recollection:: [[Install Lamp Manjaro]]
```mysql
USE mysql
SET PASSWORD FOR root@localhost='';
```

Allow phpmyadmin to logging in without password
source:: ["Password is Forbidden" PhpMyAdmin Login Error Solved - Liquid Web](https://www.liquidweb.com/kb/error-login-without-a-password-is-forbidden-by-configuration-see-allownopassword-solved/)
`/etc/webapps/phpmyadmin/config.inc.php`
```json
$cfg['Servers'][$i]['AllowNoPassword'] = true;
```


```

```