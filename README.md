# csdr-api-manager-backend

http://hackaton.ecdevops.eu/

To start the project.

* sudo docker-compose build - to rebuild the containers with new code
* sudo docker-compose up - starts the containers
* sudo docker-compose down - deletes all resources (except volumes)

## Volumes
There are two volumes created:
* mongodb_data - contains the data
* mongodb_config - contains config

Working with the MogoDB named volumes (data and config)
to list volume: 
* sudo docker volume ls

We are mapping a volume to persist over restarts. to clear the volume you can given it is a named volume do:
* sudo docker volume rm dockernodemongo_mongodb

If volume is in use you have to stop the running container, easiest is to do:
* docker-compose down