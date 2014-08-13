####backup all databases in one file (eventually add the option --add-locks):
mysqldump -u username -p -–all-databases > file.sql

####backup all databases in one gzipped file:
mysqldump -u username -p -–all-databases | gzip > file.sql.gz

####restore all databases:
mysql -u username -p < file.sql 



####Connect to Amazon RDS
`` mysql -uaamnah --password —host=db.mysite.com ``

####Creating MySQL database
`` mysql > CREATE DATABASE databasename ; ``

####Creating MySQL User
`` mysql> CREATE USER 'username'@'host' IDENTIFIED BY 'password' ; ``

####Allowing User to Connect
// grant usage on server so the user can connect  
`` mysql> GRANT USAGE ON *.* TO 'username'@'host' ; ``

####Granting Privileges
`` mysql> GRANT ALL PRIVILEGES ON databasename.* TO 'username'@'host' ; ``

####CHECK if you can connect to the created database with the user you crteated
`` mysql -uusername -p --host=mysql.hostmarkaz.com databasename  ``

####Deleting MySQL User
`` mysql> DROP USER 'username'@'host' ; ``


####Import SQL database
`` mysql -u username -p password databasename < filename.sql ``

####List all users
`` SELECT User,Host FROM mysql.user; ``

####View Users and Permissions
`` SELECT user, host, password, select_priv, insert_priv, shutdown_priv, grant_priv FROM mysql.user ``

####View User Permissions for individual Databases
`` SELECT user, host, db, select_priv, insert_priv, grant_priv FROM mysql.db ``

####Sample Command: 
`` mysqldump --user=root --password=password --host=vortex.aamnah.com wpblog | mysql --host=mysql.hostmarkaz.com --user=aamnah --password=password wpblog ``

NOTES:
---

   * If not connecting, check if the port is open on the server you are connecting from. RDS uses 3306. On KH server it couldn’t connect because the port was closed.

   * If the connection is not getting through the error would be ‘could not connect’.

   * If login is incorrect the error would be ‘access denied’. *mysql_connect(): Access denied for user*.

   * The user you are connecting with needs to be created at RDS. It doesn’t matter if the server you are connecting from has it or not.


**Opening Ports**:
Ports should be opened in the firewall configuration.

This can be accessed in WHM >> Plugins » ConfigServer Security & Firewall >> Firewall configuration >> Port settings.