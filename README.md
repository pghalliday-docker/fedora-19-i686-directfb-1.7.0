fedora-19-i686-directfb-1.7.0 
=============================

Scripts to generate a Fedora 19 i686 docker base image with DirectFB 1.7.0 installed.

To build the container
----------------------

On a machine with docker installed, pull the repository then

```
sudo docker build -rm --tag=pghalliday/fedora-19-i686-directfb-1.7.0 .
```

To run the container
--------------------

In order to launch GUI apps and use the host XServer it is necessary to map the host X11 socket to the container.
Also use linux32 so that package managers and such don't get confused about the architecture

```
sudo docker run -ti \
-e DISPLAY=$DISPLAY \
-v /tmp/.X11-unix:/tmp/.X11-unix \
pghalliday/fedora-19-i686-directfb-1.7.0 /bin/linux32
```

Then `uname -m` will report `i686`
