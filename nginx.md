---
layout: default
title: okdocker/nginx
description: Debian strech, nginx and ngx_pagespeed module, compiled as a .deb in a separate container and installed in a clean debian.
---

# okdocker/nginx

A docker image based on debian stretch containing the nginx web server with ngx_pagespeed, a web
performance module.

## Content

* Debian Stretch
* Nginx (version depends on image tag, either mainline or stable)
* ngx_pagespeed

## Usage

{% highlight console %}
$ docker run -it -p 80:80 okdocker/nginx:mainline
{% endhighlight %}

A real world example would probably use it as base image for a custom image. Here is a minimalistic working dockerfile.

You may want to override the `/etc/nginx` directory with your own configuration.

{% highlight docker %}
{% include_relative examples/nginx/Dockerfile %}
{% endhighlight %}

You can have a look at [the basic okdocker/nginx example](https://github.com/okdocker/okdocker.github.io/tree/master/examples/nginx).

## Interface

### Volumes

* `/var/cache/nginx/`: cache-related stuff for nginx; on-disk pagespeed cache should go in a subfolder.

### Ports

* HTTP (80)
* HTTPS (443)

### Paths

* `/etc/nginx/`: nginx configuration
* `/var/www/`: static files, usually one subfolder per site.

## Compile-time configuration

``` 
nginx path prefix: "/etc/nginx"
nginx binary file: "/usr/sbin/nginx"
nginx modules path: "/usr/lib/nginx/modules"
nginx configuration prefix: "/etc/nginx"
nginx configuration file: "/etc/nginx/nginx.conf"
nginx pid file: "/var/run/nginx.pid"
nginx error log file: "/var/log/nginx/error.log"
nginx http access log file: "/var/log/nginx/access.log"
nginx http client request body temporary files: "/var/cache/nginx/client_temp"
nginx http proxy temporary files: "/var/cache/nginx/proxy_temp"
nginx http fastcgi temporary files: "/var/cache/nginx/fastcgi_temp"
nginx http uwsgi temporary files: "/var/cache/nginx/uwsgi_temp"
nginx http scgi temporary files: "/var/cache/nginx/scgi_temp"
```

## Tags

* mainline (or 1.13.3): Nginx mainline version, latest version working with pagespeed.
* stable (or 1.12.1): Ngins stable version.

## Links

* [Recipe](https://github.com/okdocker/nginx)
* [Build](https://travis-ci.org/okdocker/nginx)
* [Hub](https://hub.docker.com/r/okdocker/nginx/)
* [Mirror](https://quay.io/repository/okdocker/nginx?tab=tags)
* [Nginx configuration boilerplate](https://github.com/okdocker/server-configs-nginx)



