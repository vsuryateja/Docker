

without SWARM: "docker run" vs "docker-compose" - 1 container per 1 image
	"docker run" command to run our application i.e., docker image

	docker engine - we can run one image at a time. finally, one container will be created

	"docker-compose" - yml file, we can configure more than one image details into yml file.

	required tools: 	docker engine docker-compose

with SWARM: "docker service" vs "docker stack" - more than 1 container per 1 image
	docker swarm - we can deploy our apps(only one at a time) using "docker service"

	docker engine docker swarm
	
	docker stack - deploy more than one app at a time using docker-compose

	required tools: docker engine docker swarm docker-compose
