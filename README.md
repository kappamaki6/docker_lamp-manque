# docker_lamp-manque
LAMP with phpMyAdmin using official docker images via docker-compose

___
### To Put your PHP files/folder on Apache
Comment out the volume configuration of www service
```
 volumes:
 - "Path/to/your/PHP/.:/var/www/html"
```

Path/to/your/PHP/.&emsp;&emsp;&emsp; is for putting the content of the source directory

Path/to/your/PHP/&emsp;&emsp;&emsp; is for putting the source directory

Path/to/your/PHP/hoge&emsp; is for putting the source

### To Use your mysql data
Comment out the volume configuration of db service
```
 volumes:
 - /opt/mysql_data:/var/lib/mysql
```

### To Build and run this docker
Run commands below
> &#35; Go to the directory where yaml stored.
> 
> cd /path/to/folder/
> 
> &#35; Run docker-compose with detach option.
> 
> docker-compose update -d

### To Use phpMyAdmin
Run command below
> &#35; Get MySQL docker container name
> 
> docker ps
Open browser and Type "http://localhost:8080/"
Fill out the required info
- Server:(MySQL container name):3306
- User:root
- Password:dbrootpass

### To Execute commands in a runnning container
Run commands below
> &#35; Get any docker container name you want
> 
> docker ps
> 
> &#35; Get a bash shell
> 
> docker exec -it CONTAINER_NAME /bin/bash
To quit the bash shell, Press the key below
Ctrl + p + q

### To Stop this docker
Run command below
> docker-compose down

Bye::ghost:
