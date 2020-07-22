# Demo spring-boot-docker-gcb
Demo project for Spring Boot Docker use Google Cloud Build service.

## Step 1:
Clone this repository. 
```
git clone git@github.com:habogay/spring-boot-docker-gcb.git
```

## Step 2: 
Go to the spring-boot-docker-gcb folder, and run.
```
cd spring-boot-docker-gcb
mvn clean package
```

## Step 3:
Build docker: "habogay" is reposity name. "spring-boot-docker-gcb" is image name. "." is current path.
```
docker build -t habogay/spring-boot-docker-gcb .
```

## Step 4: 
Run docker from local port 9999 
```
docker run -p 9999:8080 habogay/spring-boot-docker-gcb
```

## Step 5: 
Check docker works or not on a browser: http://localhost:9999/ . 9999 is the port that you configured.

# Push image
Push the image to the Docker Hub.
```
docker push habogay/spring-boot-docker-gcb
```
### Note:
If you don't login to Hub Docker yet, please login your hubDocker's account before push the image: docker login -u [username]
```
docker login -u habogay
```
# Pull image
## Step 1:
Pull the image from the Hub Docker.
```
docker pull habogay/spring-boot-docker-gcb
```
## Step 2:
Run the image
```
docker run -p 9999:8080 habogay/spring-boot-docker-gcb
```
