# NGINX WebDAV container

Usage:

1. Clone the repository:
```bash
git clone https://github.com/keult/webdav-nginx-docker.git
```

2. Build docker image:
```bash
cd webdav-nginx-docker
docker build . --tag webdav:1.0
```

3. Start the container:
```bash
docker run --restart always --detach --name webdav --publish 7000:8080 \
           --env WEBDAV_USERNAME=webdav_user --env WEBDAV_PASSWORD=password \
           --env UID=$UID --volume $PWD/webdav:/media webdav:1.0

```

WEBDAV_USERNAME:WEBDAV_PASSWORD for basic authentication.

