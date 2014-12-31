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

Use linux32 so that package managers and such don't get confused about the architecture

```
sudo docker run -t -i pghalliday/fedora-19-i686-directfb-1.7.0 /bin/linux32
```

Then `uname -m` will report `i686`
