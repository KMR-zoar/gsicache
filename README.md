#GSITileCache Docker File
This repository contains Dockerfile of nginx cache service Dcoker's automated build.

##Base Docker Image
+ debian:latest

##Installation
### Clone this repository

```
$ git clone https://github.com/KMR-zoar/gsicache.git
```

### Build dcoker contains

```
$ cd gsicache
$ docker build -t zoar/gsicache .
```

### Run tilecache contains
You have to be able to connect the port 8080 of contains.  
Recommended that you specify a cache directory with `-v` option.

```
$ mkdir -p /tmp/gsi/cache
$ mkdir -p /tmp/gsi/tmp
$ docker run -i -d -p 8080:8080 \
-v /tmp/gsi/cache/:/tmp/gsi/cache/ \  
-v /tmp/gsi/tmp/:/tmp/gsi/tmp/ \
-t zoar/gsicache
```
