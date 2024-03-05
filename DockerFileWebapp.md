# Create a Docker file for Apache tomcat webapp.

## Creating a docker file.

```bash
FROM tomcat:8.0-alpine
LABEL maintainer=”anand@exmaple.com”
ADD helloworld.war /usr/local/tomcat/webapps/
EXPOSE 8080
CMD ["catalina.sh", "run"]
```
Note: Make sure the helloworld.war resides in the same directory

## Baking a docker Image.
```bash
docker build -t mywebapp .
```

## Verifying the Docker image
```bash
docker image ls
```

## Creating a container image from the image.
```bash
docker run -p 8080:8080 mywebapp
```


