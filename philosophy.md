# Philosophy

Ok, Docker is a very simple project, aiming at having always up to date and uncluttered images available for some systems and/or languages/tools I use on a lot of different projects.

The goal is to generate zero toil for image maintenance, keeping them up-to-date and secure.

* Build packages, if necessary, should not be included in the final images (nor in layers).
* Rockerfiles are prefered over Dockerfiles to enable sharing artifacts between builds and having volumes available on build. The usual docker arguments against this is to say that builds must me predicatble but this is wrong, dockerfiles can download files and thus a given dockerfile can build two different containers.
* Images should be aiming production systems. Debug symbols, utilities and other artifacts that are not strictly necessary to run a system in production should be left out.
* Docker hub documentation is not very good. Each published image should at least provide a working minimalistic example of extending the image, and all volumes / ports / environment variables should be documented.

Maybe more things that I have in my head, but for now, can't think of any.