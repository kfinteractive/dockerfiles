# backup-tools

Docker Hub: https://registry.hub.docker.com/u/kfinteractive/backup-tools

This image contains a minimal arch with rsync installed. This comes in useful when backing up volumes from data containers. Example usage:

`docker run  -ti --volumes-from=data-container -v /root/backup:/backup  kfinteractive/backup-tools rsync -avz /data-volume/ /backup/`
