## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/amisfa/ex_on_lampp.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/amisfa/ex_on_lampp.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.





///////////////////////////////////////////////////////////////
//first you should run these commands in terminal:
```markdown
sudo apt-get update
sudo apt-get install php-redis build-essential libtool autoconf unzip wget mlocate
```


//and
you can use each redis version insted redis-5.3.2.tgz, check here:
https://pecl.php.net/package/redis
then you must:
wget https://pecl.php.net/get/redis-5.3.2.tgz

get link where dl this package with:
locate redis-5.3.2.tgz


if locate cant found your package link you must update database of locate whith this command(By default it is updated once in a day):
sudo updatedb

now get link and go to the file directory(you can save this file where you want, we suppos file in this link : /home/user/Downloads/lampp_extensions/redis-5.3.2.tgz
):
cd /home/user/Downloads/lampp_extensions

tar xzf redis-5.3.2.tgz
cd redis-5.3.2
phpize
./configure --with-php-config=/opt/lampp/bin/php-config
make
sudo make install


//finally add below line to /opt/lampp/etc/php.ini

extension="redis.so"


restart your xampp with this command:
sudo /opt/lampp/lampp restart

and search redis with ctrl+f in this page:
localhost/phpinfo.php






