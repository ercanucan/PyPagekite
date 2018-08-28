# PageKite owned Front-end Docker container

This Docker image can be used to run owned PageKite front-ends. It is derived from `python2.7` Docker container.

## Usage

You can download the prepared image from Docker Hub:
```
docker pull ercanucan/pypagekite
```

Example usage:
```
docker run -p PORT1:80 -p PORT2: 443 ercanucan/pypagekite --ports=80,443 --protos=http,https --domain=http,https:DOMAIN:SECRET
```

- `PORT<N>`: the ports (e.g 50443) on which the host machine will bind container's ports 80 and 443.
- `DOMAIN`: DNS name which points to the IP of the front-end relay (either an A or CNAME record).
- `SECRET`: The secret string which will be used by the PageKite back-ends in order to connect to this PageKite front-end.

## Build your own

You can build the container as usual with the following command:
```
docker build -t <container-name> .
```
