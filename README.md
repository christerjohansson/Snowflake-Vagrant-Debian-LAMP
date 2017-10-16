# Snowflake Vagrant LAMP stack with Webmin
VagrantBox with a complete LAMP-stack based on Debian 9.

# Features
- Complete LAMP stack
- PHP 7.1 &PHP5.6
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
