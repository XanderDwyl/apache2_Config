# Backup Configuration
	- http-vhosts.conf 
	- http.conf 

# How to install php without using port or brew

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