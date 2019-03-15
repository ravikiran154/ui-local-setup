# ui-local-setup(requires Gcloud access)

gcloud auth configure-docker

Install docker and docker-compose

Follow below steps before launching

1. docker-compose down
2 .docker-compose -f docker-compose-dev-db.yml up -d

finally run "docker container ls" to check if all the services are up and running


To get the latest image, get the SHA id from build step and use it in the docker-compose file


UI project configuration:

1. disable redirection to user-service in the router module.
2. Use static auth token to resolve roles and permissions


LOCAL DB set up instructions:

goto gcloud console --> Navigation menu --> storage--> dev_dumps-->download dev dump --> rename it to "osdashboard.sql" and put it in dumps folder

Follow below steps before launching

1. docker-compose down
2. sudo docker volume ls -qf dangling=true
3. sudo docker volume rm $(sudo docker volume ls -qf dangling=true)
4. docker-compose up

docker inspect --format='{{json .State.Health}}' mysql

verify json until status is changed to healthy and exit code is 0

finally run "docker container ls" to check if all the services are up and running

To get the latest image, get the SHA id from build step and use it in the docker-compose file


