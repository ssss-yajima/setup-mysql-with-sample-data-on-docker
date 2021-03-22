# Set up MySQL with sample data on docker

## SetUp MySQL Container

1. (If necessaly)Modify  `docker-compose.yml`
2. Run mysql container:  
`docker-compose up -d`
3. Confirm the container:  
`docker ps`

## Import sample data to mysql

1. Download sample data from here  
[MySQL :: Other MySQL Documentation](https://dev.mysql.com/doc/index-other.html)
2. Copy downloaded file to the container:  
`docker cp test_db-1.0.7.tar.gz mysql_docker:./`
3. Unzip sample data:  
`tar -zxvf test_db-1.0.7.tar.gz`
4. Move to unzipped folder.  
`cd test_db`
5. Import sample data to MySQL.  
`mysql -u root -p < employee.sql`

## Connect from VSCode SQLTools extention

1. Instal VSCode extentions [SQLTools](https://vscode-sqltools.mteixeira.dev/?umd_source=repository&utm_medium=readme&utm_campaign=mysql) and [SQLTools MySQL/MariaDB](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools-driver-mysql)
2. Open SQLTools window from side bar.
3. Input connection settings like bellow image.
4. Press `SAVE CONNECTION` and confirm that tables and views are listed on SQLTools menu.

[![Connection settings](https://i.gyazo.com/618b9e1a4fedeb88aae5bb1cafb2797a.png)](https://gyazo.com/618b9e1a4fedeb88aae5bb1cafb2797a)

[![Tables and views on SQLTools menu](https://i.gyazo.com/67c976e9cfcd9baf5c5b6a937d9b5e8b.png)](https://gyazo.com/67c976e9cfcd9baf5c5b6a937d9b5e8b)
