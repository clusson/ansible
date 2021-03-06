# Ansible config

We're using Centos as distrib hosted on [Scaleway](https://www.scaleway.com/).

## Roles : 
* __Common__
  * Update packages
  * Install
    * yum-utils
    * policycoreutils-python
    * wget
    * epel-release
    * git
    * firewalld
  * Confgure
    * firewalld
    * selinux
  * Reboot
* __Java__
  * Install OpenJDK 1.8
* __Jenkins__
  * Add repo & key
  * Install, start & enable
  * Set configuration
* __MySQL__
  * Install MariaDB
  * Update root credentials
  * Create *ansible* db & user
* __Nginx__
  * Install
  * Deploy configuration
  * Configure firewalld for *http* & *https*
* __PHP__
  * Install
    * php70
    * php70-php-fpm
    * php70-php-pecl-mysql
  * Configure php-fpm
* __VHost__
  * Create .conf
    * Set up reverse proxy vhost + ssl certificate
    OR
    * Set up PHP-FPM vhost
  * Generate certificates
  * Set domain vhost
