# Docker Meetup Bamberg
## Docker on Windows

## Online

* http://stefanscherer.github.io/talks/20161117_DockerMeetupBamberg_DockerOnWindows

## Container

You can run the slides as a Windows container. Currently I use IIS for the static files. But I think I will create a smaller image in the future.

```
docker run --rm --name=dockerbamberg -p 8000:8000 -d stefanscherer/talks:2016-11-17
```

Open a browser

```
start http://$(docker inspect -f '{{ .NetworkSettings.Networks.nat.IPAddress }}' dockerbamberg):8000
```

### Description for Remark Markdown

* https://github.com/gnab/remark/wiki/Markdown

