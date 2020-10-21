# Docker-realvnc-vnc-viewer

Minimal docker image containing [RealVNC VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/linux/). nothing more, nothing less

# Docker Hub

Find the docker image here: https://hub.docker.com/r/adanrehtla/docker-realvnc-vnc-viewer

# Usage

Open RealVNC VNC Viewer:

`docker run -d --rm --net=host -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/home/vnc/.Xauthority -e DISPLAY=$DISPLAY -h $HOSTNAME adanrehtla/docker-realvnc-vnc-viewer:latest`

Connect RealVNC VNC Viewer to a VNC Server:

`docker run -d --rm --net=host -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/home/vnc/.Xauthority -e DISPLAY=$DISPLAY -h $HOSTNAME adanrehtla/docker-realvnc-vnc-viewer:latest 127.0.0.1:5900`

## CLI Options

A full list can be found here:

`docker run adanrehtla/docker-realvnc-vnc-viewer:latest --help`
