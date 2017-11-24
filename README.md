## Docker configuration template for Noetic backend applications deployment


Modify .env file specifying details as per your specific environment.

**LOCAL_WAR_DIR_PATH** = maven target folder or any path that contain your WAR. Note that this is an host OS specific path.

#### to Build
```
docker-compose build
```

#### to Run
```
docker-compose up
```
#### <i class="icon-file"></i> Note
> - Remote debugging is enabled via port 8787. You may use that port to connect from your IDE.
> - Inital DB dump is included in the ./mysql/tomcat/init_dump.sql




 **Tip:** 
For Hospitality API, **TARGET_DOCKER_TOMCAT_WAR_PATH** should be the following so that it resolves imperial-api to root context :
	```/usr/local/tomcat/webapps/ROOT```
	
For other APIs you may just specify webapps directory
    ```/usr/local/tomcat/webapps```