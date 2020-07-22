# spring-boot-docker-gcb
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
Check docker works or not on a browser: http://localhost:9999/ . 9999 is the porthat you configured.

