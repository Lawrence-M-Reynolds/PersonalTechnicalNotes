# Command aliases
## Stop all containers
dockerStopAll
alias dockerStopAll='docker stop $(docker ps -a -q)'

# General docker
## Log into container
docker exec -it 0f3e311a89fd bash

## copy to container
docker cp /mnt/c/Users/fileToUpload.txt {CONTAINER_ID}:/var/fileToUpload.txtw

## Follow log output
docker logs -f {CONTAINER_ID}

You can also use the id from intllij:
docker logs -f b01d5f2e7d5d13bbd16b69b2b64a425ac92403b875c3e78905ad371e1ad409f5