# HelloMySQL-PHP
Example Machine Learning with MySQL via PHP with Apache2 

#### Requires
- Apache2
- php7.1-mysql
- php7.1
- PHP-ML (0.6+)

If you did want to run this yourself without tinkering, you should install PHP-ML using composer as in
their guide and set up MySQL to look for files in /var/lib/mysql-files/,
have apache2 look for html in /var/www/html/ and also store a dbconfig.php
```php
<?php
    $host = 'localhost';
    $dbname = 'Youtube';
    $username = 'root';
    $password = 'yourpassword';
?>
```
in you home/bin/. Then when ready run
```bash
./UpdateSQLDataBase.sh && ./deploy
```
deploy will attempt to open localhost in firefox so change that if you want.

Note there's a
```php
// because ML...
<?php ini_set('memory_limit','4096M'); ?>
```
in YoutubeSQL.php since the data is so large, even with just using the first 1000 rows!


- Using [Youtube trending data from Kaggle](https://www.kaggle.com/datasnaek/youtube-new) 
- Forming a MySQL database with a bash generated script
- Doing some basic MLP classification from tokenised descriptions and some other simple attributes to
  detemine the category and some other things
- Using [PHP-ML](https://php-ml.readthedocs.io/en/latest/) to do the machine learning because why not learn some more PHP
###### Youtube Data ML
![youtube](https://github.com/harveydevereux/HelloMySQL-PHP/blob/master/pics/sql.png)
#### Some Screenshots
###### Clustering
![clustering](https://github.com/harveydevereux/HelloMySQL-PHP/blob/master/pics/cluster.png)
###### Regression
![regression](https://github.com/harveydevereux/HelloMySQL-PHP/blob/master/pics/reg.png)
