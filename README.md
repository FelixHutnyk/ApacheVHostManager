# Apache Vhost Manager

Forked & Modified From [vhost-manager](https://github.com/rubensfernandes/vhost-manager)


#Usage

First install script

```sh
git clone https://github.com/CodingMachineDev/ApacheVHostManager.git
cd apache-vhost-manager
chmod 777 vhost
./vhost -install
```

**Add vhost test.com**
```sh
$ sudo vhost -r /var/www/test.com -url 'test.com' 'test.com'
```
>'test-site' is a name of config ex: /etc/apache2/sites-available/test-site.conf

To use a specific template
```sh
$ sudo vhost -r /var/www/test-site.com -url 'test-site.com' -t ~/template.conf 'test-site'
```
- **-r** is a directory
- **-url** is the url to load
- **-t** is the template file
- **-p** the port which the website will be hosted
- **test-site** is name of config to set in /etc/apache2/sites-available/mysite.conf

>Templates should use the following parameters:
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
