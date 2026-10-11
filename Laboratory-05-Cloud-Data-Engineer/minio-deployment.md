The following information is technical information regarding the process of running a docker container with MinIO.

### DISCLAIMER ⚠️
> The original `minio/minio` docker image was completely removed from DockerHub. This also applies to `quay.io/minio/minio` and `bitnami/minio`. This is due to MinIO having completely discontinued their open-source Community Edition (CE) containers as a way to shift to monetization. Due to this, a replacement was needed. This documentation will instead be using `pgsty/minio`, aka SILO (S3 Interface - Libre Object Store), a maintained open-source fork and continuation of the MinIO open-source Community Edition container lead by Pigsty (PostgreSQL In Great STYle). The steps fortunately still remains the same as if MinIO is still being used.

# Commands 🖥️
```
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
-e "MINIO_ROOT_USER=cloudadmin" \
-e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
pgsty/minio server /data --console-address ":9001" 
```

The following will provide explanations to the command.
- `docker run` - Used to run containers. Can also be used to create new containers.
    - If the image does not exist locally, it will pull the image from DockerHub and download it.
- `-d flag` - Detached mode. Allows for the container to run in the background.
- `-p flag` - Port. Specifies which port the container will run in.
    - The following port used within the command was port 9000 and 9001
- `--name flag` - Self explanatory. Provides custom name to container.
- `-e flag` - Environmental variables. Allows you to set environmental variables.
    - `MINIO_ROOT_USER` allows you to set the username of the root user. In this case, we set it to `cloudadmin`.
    - `MINIO_ROOT_PASSWORD` allows to set the root password for your root user. This allows for more security so the root user can't easily be logged into.
- `--console-address` - Specific for MinIO/SILO. Provides a hostname and port on which the MinIO/SILO web console will listen from.
    - In our case, while the ports 9000 and 9001 is taken, the console address will mostly listen to the user within port 9001.

# MinIO/SILO Buckets 🪣
Buckets are essentially your storage directories or top level containers for objects. In this case, the bucket being made is for the images of clients, therefore it is named `client-images`. These will serve as the container or directory for images sent in by clients.