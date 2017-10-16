# Snowflake Vagrant LAMP stack with Webmin
VagrantBox with a complete LAMP-stack based on Debian 9.

# Features
- Complete LAMP stack
- PHP 7.1 (default), 7.0 & 5.6
- MariaDB
- Redis
- Composer
- PHPUnit
- WP-CLI
- Webmin 1.860

# Webmin Control Panel
Webmin is a web-based interface for system administration for Unix. Using any modern web browser, you can setup user accounts, Apache, DNS, file sharing and much more. Webmin removes the need to manually edit Unix configuration files like /etc/passwd, and lets you manage a system from the console or remotely.

(Feel free to install Vagrant Hostsupdater-plugin for easier use of hostnames)

# INSTALLATION
1. Clone this repository
2. Edit Vagrantfile according to your project (IP-adress, memory etc)
3. Run the command Vagrant up in your console
4. Your box is now available at your chosen hostname or ip.
5. To manage your settings, go to https://[YOUR_HOSTNAME_HERE]:10000 (ie. https://snowflake.dev:10000)
6. The world is your oyster!

# SSH
Enter Vagrant SSH in your console to access the box through SSH. You can also use PuTTy or similar programs to SSH into the box. Host IP is as entered in the Vagrantfile. Username is vagrant and password is vagrant.

# Changing PHP versions
By default 7.1 is activated. To change back to for example 5.6, enter the Webmin panel and visit System Software Packages, choose to install from APT. Search for libapache2-mod-php5.6, and it will add all dependency packages as well. Then visit Others-->PHP Configuration and set the correct values for your chosen php version. You will need to adjust the module configuration by clicking the link and edit the values. PHP 7.1 is located in the folder /etc/php/7.1 and 5.6 is in /etc/php/5.6.

Then just click save and you will be given access to the php.ini file for the selected version.
To activate PHP5.6 you need to visit Servers--> Apache Server --> Configure Apache Modules and activate PHP5.6 module, remember to de-activate php7.1 module. You can not run 7.1 and 5.6 simultaneously.
