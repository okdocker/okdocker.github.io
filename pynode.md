---
layout: default
title: okdocker/pynode
description: Debian, Python and Node.js docker image, built daily on travis. Contains Yarn for Node.js package management.
---

# okdocker/pynode

A docker image that bundles both modern Python interpreter and Node.js, with Yarn.

## Content

* Debian Jessie
* Python 3.6 (will stay on latest stable python 3)
* Node.js (LTS or Current)
* Yarn

## Usage

{% highlight console %}
$ docker run -it okdocker/pynode:latest /bin/bash
{% endhighlight %}

Application code should go into the `/app` default working directory, image do not use volumes and expose no ports.

## Tags

* lts (or 3.6-6.x): Node.js LTS
* latest (or 3.6-8.x): Node.js Current

## Links

* [Recipe](https://github.com/okdocker/pynode)
* [Build](https://travis-ci.org/okdocker/pynode)
* [Hub](https://hub.docker.com/r/okdocker/pynode/)