# Docker Meetup Bamberg
## Docker on Windows

## Online

* http://stefanscherer.github.io/talks/20161117_DockerMeetupBamberg_DockerOnWindows

## Container

You can run the slides as a Windows container.

### Run container
```
docker run --rm --name=dockerbamberg -p 8080:8080 -d stefanscherer/talks:2016-11-17
```

Open a browser

```
start http://$(docker inspect -f '{{ .NetworkSettings.Networks.nat.IPAddress }}' dockerbamberg):8080
```


### Build image with IIS

The IIS image is based on microsoft/windowsservercore.

```
docker build -t stefanscherer/talks:2016-11-17 -f Dockerfile.iis .
```

### Build image with minimal webserver

My minimal webserver is only 5 MByte and based on microsoft/nanoserver.

```
docker build -t stefanscherer/talks:2016-11-17 .
```

### Description for Remark Markdown

* https://github.com/gnab/remark/wiki/Markdown
