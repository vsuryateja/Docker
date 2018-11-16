docker swarm init
it will give you join command. past it in nodes.

create overlay network 

docker network create s-overlay -d overlay

docker service create --name jenkins --network s-overlay --replicas 3 -p 8080:8080 jenkins

docker service ps jenkins

you check chen containers in another docker mechine also.

you can launch jenknis with any ip address with port 8080.

remove service:
 docker service rm jenkins
scale service.
 docker service scale jenkin=5
inspect:
 docker service inspect jenkins

what is the use of overlay network?
when you initialize a swarm or join a Docker host to an existing swarm, two new networks are created on that Docker host:
	> an overlay network called ingress, which handles control and data traffic related to swarm services. When you create a swarm service and do not connect it to a user-defined overlay network, it connects to the ingress network by default.
	> a bridge network called docker_gwbridge, which connects the individual Docker daemon to the other daemons participating in the swarm.
	more info at https://docs.docker.com/network/overlay/#operations-for-all-overlay-networks