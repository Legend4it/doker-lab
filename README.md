# doker-lab
Test docker command and imeges

//List all images
> docker images

//Build Image: -t <image name>:tag .
> docker build -t docker-demo:1.0.0 .

//Check Our build image
> docker images

//Check images history
> docker history ac66

// When run docker image create a container: 
// Tack image and build on top of image. 
// When remove containder all image will distroy. should update not distroy

//Run in disconnected mode: docker run --name <name> -p machin/local-port:container-port <image name>
> docker run --name container-demo -p 8080:80 docker-demo:1.0.0

//Show images
>docker images

//Show containers -a show all container run and not run
>docker ps -a

//Stop runing container: docker stop <id>
>docker stop a2e6

//Start container: docker start <id>
>docker start a2e6


//To remove container: docker rm <id>
>docker stop a2e6
>docker rm a2e6

//Update image by create new one because image is read only. -t is tag
>docker build -t docker-demo:1.0.1 .

//Run the container with disconnected mode -d
>docker run -d --name container-demo -p 8080:80 docker-demo:1.0.0

//Can run sam image in old version on other container
>docker run -d --name container-demo -p 8080:80 docker-demo:1.0.0
>docker run -d --name container-demo-01 -p 8080:80 docker-demo:1.0.1

//Stop multi container: docker stop <id-01> <id-02>
>docker stop e9cae9caa8686d21 54469d216cf9
