### Building and running your application

When you're ready, start your application by running:
`docker compose up --build`.

### Deploying your application to the cloud

First, build your image, e.g.: `docker build -t myapp .`.
If your cloud uses a different CPU architecture than your development
machine (e.g., you are on a Mac M1 and your cloud provider is amd64),
you'll want to build the image for that platform, e.g.:
`docker build --platform=linux/amd64 -t myapp .`.

Then, push it to your registry, e.g. `docker push myregistry.com/myapp`.

Consult Docker's [getting started](https://docs.docker.com/go/get-started-sharing/)
docs for more detail on building and pushing.

Notes.

Docker compose is building and running image

-start server
-run docker run -p 8080:8080 flappygameslv/spring-app

-create new build and push to docker hub

>docker build --tag flappygameslv/spring-app .
> 
>docker push flappygameslv/spring-app:tagname
> 
> `docker pull flappygameslv/spring-app  (in server)`
> 
> `docker stop springboot-server`
> 
> 
> 
` docker run --rm  \
--name springboot-server \
--network mysqlnet \
-e MYSQL_URL=jdbc:mysql://mysqlserver/petclinic \
-e SPRING_PROFILES_ACTIVE=mysql \
-p 8080:8080 flappygameslv/spring-app`

