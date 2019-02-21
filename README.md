# ui-local-setup(requires Gcloud access)

gcloud auth configure-docker

Install docker and docker-compose



Follow below steps before launching

1)docker-compose down
3)sudo docker volume ls -qf dangling=true
3)sudo docker volume rm $(sudo docker volume ls -qf dangling=true)
4)docker-compose up