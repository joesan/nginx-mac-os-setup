To run nginx as a docker container, do the following steps:

1. Add the following content and save it as Dockerfile
   ```
    Set nginx base image
    FROM nginx

    # File Author / Maintainer
    MAINTAINER YourName "youremail"

   # Copy custom configuration file from the current directory
   COPY nginx.conf /etc/nginx/nginx.conf
   ```
Make sure you have the nginx.conf located in the same folder that contains this Dockerfile

2. Assuming that you have docker installed, do the following to build the image after navigating to the folder that contains
   newly created Dockerfile
   
    ```docker build -t joesan:nginx-latest . ```
    
    where -t specifies the reposiroty:tagname for the image that you want to build

3. Now check if the image is successfully built using the following command:
   
   docker images
   
   it should show you the newly created image. For example., on my machine I see the following:
   
   ```
   Joesans-MacBook-Pro:nginx-docker jothi$ docker images
   REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
   joesan              nginx-latest        0d73419e8da9        3 seconds ago       182.8 MB
   hello-world         latest              c54a2cc56cbb        13 days ago         1.848 kB
   nginx               latest              0d409d33b27e        6 weeks ago         182.8 MB
   ```
   
4. To start this image as a docker container, issue the following command

   
   
   
   
