---
layout: default
---

# Frequently Asked Questions

## Why «yet again another» base image for ...?

In my opinion, there is a lot of problems with the variety of images available out there. Although docker hub promotes transparency, the lack of informations about how the images were actually built is problematic. It's not true for automated builds, but often it's hard to build real-world images using dockerfiles (hence our usage of rockerfiles).

The recipes for okdocker images are simple and open, and the travis ci daily builds use just that. The daily builds also ensure that the images are always rebuilt using the latest debian updates, making sure that no system package is outdated by more than 24 hours.

## Why Rocker and Rockerfiles?

Dockerfiles are a way to build reproducible and predictable builds. At least in theory. But in practice, that's not true, as it can depends on external resources provided by the network. It has been a great argument over the last few years not to push forward the dockerfile language, but it does not stand. Rocker is trying to push this language forward, and imho does it in a reasonable way. Being able to mount volumes for caching, build more than one image at once to use "build" containers to create artifacts that are used in actual "runtime" containers is a must-have in many real world situations, and that's the main reasons why we use it. 

Even if you do not use Ok, Docker images, you should definately look at rocker. It... Rocks!

## How can I trust your builds?

The simple answer is you shouldn't.

The build process is completely transparent, use a third party (travis) to build and push images to the hubs, so maybe you can consider that's enough for you, but if your paranoid (and on the internet, you should be), just clone the recipe repositories of the image you need, inspect it, hack it, and then use it on systems you really trust.
