# Ubuntu 14.04 System Admin Commands


## Ubuntu_Commands

### Open Chrome from terminal 
* `google-chrome-stable` --- use that command in the terminal 


### History Command overview 
* We use `history` command to check history of all commands which we use in terminal
* maximum 2000 history command is store in .bash profile by default
* `history`

### Network troubleshooting   
* `ping yahoo.com` ---f or checking your network is connected to internet is not or DNS is working or not

###  Lamp installation
   *   `sudo apt-get update`
   *   `sudo apt-get install apache2`
   *   `echo "ServerName localhost" | sudo tee /etc/apache2/conf-available/servername.conf`
   *   `sudo a2enconf servername`
     * is  a  script  that  enables the specified configuration file
     * within the apache2 configuration
   *   `sudo service apache2 restart`
   *   `curl http://icanhazip.com`
     * The command is designed to work without user interaction.
   * `apt-get install curl`
 
   *   `sudo apt-get install mysql-server php5-mysql`
   *   `sudo mysql_install_db`
   *   `sudo mysql_secure_installation`
   *   `sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt`
   *   `sudo nano /etc/apache2/mods-enabled/dir.conf`
   *   `sudo service apache2 restart`
   *   `cd /var/www/html`
   *   `ls`
   *  `touch index.php`
     * to create new, empty files
   *   `sudo touch index.php`
   *  `ls`

   *   `sudo vi index.php`
     * for editing file in vi editor
   *   `cat index.php`
     * It has three related functions with regard to text files: 
     * displaying them, combining copies of them and creating new ones
* lamp installation completed
   *   `nano index.php` (its a small text editor)
   *  `man vi`(linux command on terminal)
   *   `history`
### installing chrome via terminal
   *   `sudo apt-get install libxss1 libappindicator1 libindicator7`
   *   `wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`
   *   `sudo dpkg -i google-chrome*.deb`
* chrome installation complete


### wordpress installation
   *   `wget http://wordpress.org/latest.tar.gz`(download wordpress)
   *   `tar -xvzf latest.tar.gz`(unzip)
   *   `sudo mv wordpress/* /var/www/html/`(move folder to required place )
   *   `mysql -u root -p`(entering in database)
   *   `sudo vi /var/www/html/wp-config.php`(edit file with vi)
   *   `sudo chmod -R 755 /var/www/html/`(running file)
   *   `sudo service apache2 restart`(restarting server)
   *   `/etc/apache2/sites-available/wordpress.conf`
   *   `sudo rm /var/www/html/wp-config.php`(removing copied file)
   *   `sudo cp /var/www/html/wp-config-sample.php /var/www/html/wp-config.php`(copy file with name change)

   *   `ls` (checking list)
   *   `sudo service apache2 restart`
   *   `sudo vi /var/www/html/wp-config.php`
   *   `sudo chown -R www-data:www-data /var/www/html/`(changing ownership of specified file)
   *   `sudo chmod -R 755 /var/www/html/`
   *   `sudo service apache2 restart`
 
   *   `mysql -u root -p`
   *   `sudo vi /var/www/html/wp-config.php`
   *   `ls`
 
   *  ` sudo rm index.html`

   *   `sudo /etc/init.d/apache2 stop`(stopping apache server)
 * wordpress installation complete
### nginx installation
  *   `sudo apt-get update`
  *   `sudo apt-get install nginx`
  *   `sudo apt-get install php5-fpm php5-mysql`
### configuration
  *   `sudo vi /etc/php5/fpm/php.ini`
  *   `readlink -f cgi.fix_pathinfo`
  *   `sudo vi /home/adnan/cgi.fix_pathinfo`
  *  ` sudo vi /etc/php5/fpm/php.ini`
  *   `sudo service php5-fpm restart`
  *   `sudo vi /etc/nginx/sites-available/default`
  *   `sudo service nginx restart`
  *  ` cd /usr/share/nginx/html`
  *   `ls`
  *   `sudo rm 50x.html` 
  *   `sudo rm index.html` 
  *   `mv wordpress /usr/share/nginx/html`
  *   `ls`
  *   `ls /var/www/html`(path of wordpress folder)
  *   `cd /var/www`
  *   `sudo cp -r html /usr/share/nginx/html`(copies files recursively of folder to given path )
  *   `cd /usr/share/nginx/html`(change directory where files copied)
  *  ` ls`
  *   `sudo rmdir html`(remove html dir)
