create Docker file which take nexusip as build arg.
create dcoker compose file to build docker image.
    in build section we can defile build arg with static value or just defile in .env file which contains key=value format.
    i created compose file for dynamic value of ip which we need to store in .env file.
run> docker-compose up
