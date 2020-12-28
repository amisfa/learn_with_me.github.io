

#Vahid



First you should run these commands in terminal and install these packages:
```markdown
sudo apt-get update
sudo apt-get install php-redis build-essential libtool autoconf unzip wget mlocate
```



You can use each redis version insted redis-5.3.2.tgz, check here:[pecl.php.net](https://pecl.php.net/package/redis)
then you must download redis-5.3.2.tgz with this command:
```markdown
wget https://pecl.php.net/get/redis-5.3.2.tgz
```

Get link where this package is with:
```markdown
locate redis-5.3.2.tgz
```


If locate can't found your package link you must update database of locate whith this command(By default it is updated once in a day):
```markdown
sudo updatedb
```

Now get link and go to the file directory(you can save this file where you want, we suppos file in this link : /home/user/Downloads/lampp_extensions/redis-5.3.2.tgz
):
```markdown
cd /home/user/Downloads/lampp_extensions
```

```markdown
tar xzf redis-5.3.2.tgz
cd redis-5.3.2
phpize
./configure --with-php-config=/opt/lampp/bin/php-config
make
sudo make install
```

Finally add below line to /opt/lampp/etc/php.ini
```markdown
extension="redis.so"
```

Restart your xampp with this command:
```markdown
sudo /opt/lampp/lampp restart
```
And search redis with ctrl+f in this page:
```markdown
localhost/phpinfo.php
```




