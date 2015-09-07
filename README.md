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
   * 5  sudo apt-get update
   * 6  sudo apt-get install apache2
   * 7  echo "ServerName localhost" | sudo tee /etc/apache2/conf-available/servername.conf
   * 8  sudo a2enconf servername
     * is  a  script  that  enables the specified configuration file
     * within the apache2 configuration
   * 9  sudo service apache2 restart
   * 10  curl http://icanhazip.com
     * The command is designed to work without user interaction.
   * 11  apt-get install curl
 
   * 14  sudo apt-get install mysql-server php5-mysql
   * 15  sudo mysql_install_db
   * 16  sudo mysql_secure_installation
   * 17  sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt
   * 18  sudo nano /etc/apache2/mods-enabled/dir.conf
   * 19  sudo service apache2 restart
   * 20  cd /var/www/html
   * 21  ls
   * 22  touch index.php
     * to create new, empty files
   * 23  sudo touch index.php
   * 24  ls

   * 26  sudo vi index.php
     * for editing file in vi editor
   * 27  cat index.php
     * It has three related functions with regard to text files: 
     * displaying them, combining copies of them and creating new ones
* lamp installation completed
   * 28  nano index.php (its a small text editor)
   * 29  man vi(linux command on terminal)
   * 30  history
* installing chrome via terminal
   * 31  sudo apt-get install libxss1 libappindicator1 libindicator7
   * 32  wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
   * 33  sudo dpkg -i google-chrome*.deb
* chrome installation complete


* wordpress installation
   * 64  wget http://wordpress.org/latest.tar.gz(download wordpress)
   * 65  tar -xvzf latest.tar.gz(unzip)
   * 66  sudo mv wordpress/* /var/www/html/(move folder to required place )
   * 67  mysql -u root -p(entering in database)
   * 68  sudo vi /var/www/html/wp-config.php(edit file with vi)
   * 69  sudo chmod -R 755 /var/www/html/(running file)
   * 70  sudo service apache2 restart(restarting server)
   * 73  /etc/apache2/sites-available/wordpress.conf
   * 79  sudo rm /var/www/html/wp-config.php(removing copied file)
   * 80  sudo cp /var/www/html/wp-config-sample.php /var/www/html/wp-config.php(copy file with name change)

   * 86  ls (checking list)
   * 115  sudo service apache2 restart
   * 116  sudo vi /var/www/html/wp-config.php
   * 117  sudo chown -R www-data:www-data /var/www/html/(changing ownership of specified file)
   * 118  sudo chmod -R 755 /var/www/html/
   * 119  sudo service apache2 restart
 
   * 122  mysql -u root -p
   * 123  sudo vi /var/www/html/wp-config.php
   * 124  ls
 
   * 126  sudo rm index.html

   * 129  sudo /etc/init.d/apache2 stop(stopping apache server)
 * wordpress installation complete
* nginx installation
  * 131  sudo apt-get update
  * 132  sudo apt-get install nginx
  * 133  sudo apt-get install php5-fpm php5-mysql
* configuration
  * 135  sudo vi /etc/php5/fpm/php.ini
  * 136  readlink -f cgi.fix_pathinfo
  * 137  sudo vi /home/adnan/cgi.fix_pathinfo
  * 138  sudo vi /etc/php5/fpm/php.ini
  * 139  sudo service php5-fpm restart
  * 142  sudo vi /etc/nginx/sites-available/default
  * 143  sudo service nginx restart
  * 144  cd /usr/share/nginx/html
  * 145  ls
  * 147  sudo rm 50x.html 
  * 149  sudo rm index.html 
  * 150  mv wordpress /usr/share/nginx/html
  * 155  ls
  * 156  ls /var/www/html(path of wordpress folder)
  * 157  cd /var/www
  * 158  sudo cp -r html /usr/share/nginx/html(copies files recursively of folder to given path )
  * 159  cd /usr/share/nginx/html(change directory where files copied)
  * 160  ls
  * 163  sudo rmdir html(remove html dir)
