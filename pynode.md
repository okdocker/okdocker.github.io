---
layout: default
title: okdocker/pynode
description: Debian, Python and Node.js docker image, built daily on travis. Contains Yarn for Node.js package management.
comments: true
---

# okdocker/pynode

A docker image based on debian jessie that bundles both modern Python interpreter and Node.js, with Yarn.

<div class="addthis_inline_share_toolbox"></div><br/>

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

A real world example would probably use it as base image for a custom image. Here is a minimalistic working dockerfile.

{% highlight docker %}
{% include_relative examples/pynode/Dockerfile %}
{% endhighlight %}

You can have a look at [the basic okdocker/pynode example](https://github.com/okdocker/okdocker.github.io/tree/master/examples/pynode).

## Tags

* lts (or 3.6-6.x): Node.js LTS
* latest (or 3.6-8.x): Node.js Current

## Links

* [Recipe](https://github.com/okdocker/pynode)
* [Build](https://travis-ci.org/okdocker/pynode)
* [Hub](https://hub.docker.com/r/okdocker/pynode/)
* [Mirror](https://quay.io/repository/okdocker/pynode?tab=tags)
