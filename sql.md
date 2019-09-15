# My SQL #
## Start & Stop MySql ##
  * ``` systemctl start mysql ```
  * ``` mysql -u 'root' -p ``` Default password is root
  * ``` systemctl stop mysql ```

## Create Database
  * ``` Create database db_name ```

## Backup Database              
  * ``` mysqldump --databases db1 db2 db3 > dump.sql ```
  * ``` mysql db_name < backup-file.sql ```

## Restore Data from Mysql Dump
  * ``` mysql -u root -p ``` Then press enter and enter password
  * ``` source filename.sql ``` To create database from dump file
