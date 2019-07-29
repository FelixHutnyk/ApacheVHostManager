# Apache Vhost Manager

Rebuild of [vhost-manager](https://github.com/rubensfernandes/vhost-manager)


#Usage

First install script

```sh
$ git clone https://gitlab.com/CodingMachine/apache-vhost-manager.git
$ cd apache-vhost-manager
$ sudo ./vhost -install
```

**Add vhost test.com**
```sh
$ sudo vhost -r /var/www/test.com -url 'test.com' 'test-site'
```
>'test-site' is a name of config ex: /etc/apache2/sites-available/test-site.conf

To use a specific template
```sh
$ sudo vhost -r ~/projects/mysite/web -url 'mysite.dev' -t ~/template.conf 'mysite'
```
- **-r** is a directory
- **-url** is the url to load
- **-t** is the template file
- **-p** the port which the website will be hosted
- **test-site** is name of config to set in /etc/apache2/sites-available/mysite.conf

>Templates should be use parameters
* template.url
* template.webroot
* template.email
* template.logpath
* template.port


To remove a virtual host use
```sh
$ sudo vhost -rm test-site
```

To see help
```sh
$ sudo vhost -h
```
