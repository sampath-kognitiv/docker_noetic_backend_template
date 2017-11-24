## Docker env setup template for Noetic backend applications deployment

A Tomcat + MySQL Setup for local development of backend projects.

**Before you begin**
1. Make sure you have installed docker and docker-compose for your OS.
2. Clone this repository and go to your working directory.
3. Modify .env file specifying details as per your specific development/OS environment.

> **LOCAL_WAR_DIR_PATH** = maven target folder or any path that contain your WAR. Note that this is an host OS specific path.



##### to Build
```
docker-compose build
```

##### to Run
```s
docker-compose up
```
#### <i class="icon-file"></i> Notes
> - Remote debugging is enabled via port 8787. You may use that port to connect from your IDE.
> - Inital DB dump is included in the ./mysql/tomcat/init_dump.sql
> - MySql DB is accessible via localhost:3306 user: root with an empty password. 
> - Following containers would be available when this setup is up and running: <br/>
	**noetic_mysql**	 <br/>
	**noetic_tomcat**
	
You may connect to a container and do inspections using:
```
	docker exec -it [container_name] /bin/bash 
```

 **Tips:** 
For Hospitality API, **TARGET_DOCKER_TOMCAT_WAR_PATH** should be the following so that it resolves imperial-api to root context :
	```/usr/local/tomcat/webapps/ROOT```
	
For other APIs you may just specify webapps directory:
    ``` /usr/local/tomcat/webapps ```
