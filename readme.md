# Backup Configuration
	- http-vhosts.conf
	- http.conf

# <a href="http://stackoverflow.com/questions/14595841/installing-mcrypt-extension-for-php-on-osx-mountain-lion/21803286?sgp=2#21803286"> How to install php without using port or brew</a>
	credited <a href="http://stackoverflow.com/users/1664755/will-palmer">Will Palmer</a>

# How to install mysql
	- brew install mysql
	- ln -sfv /usr/local/opt/mysql/*.plist ~/Library/LaunchAgents
	- mysql.server start

# Link mysql with current php running

	- Symlink mysql.sock : ln -s /tmp/mysql.sock /var/mysql/mysql.sock

# Update mysql password
	- Login: mysql -uroot
	- run this command below:

		mysql> UPDATE mysql.user SET Password=PASSWORD('test')
	    	-> WHERE User='root' AND Host='localhost';

		mysql> FLUSH PRIVILEGES;
