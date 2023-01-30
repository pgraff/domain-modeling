# Domain Modeling

## Introduction

This repo contains some files used as part of the teaching of domain modeling techniques.

## Docker

You need to install docker to use the the domain modeling tools.
At the time of writing, the correct URL to fetch Docker is https://docs.docker.com/get-docker/.

However, if the link above is broken, you should be able to do a simple Google search on the net on `how to install docker`.

## Content

- `docker-compose.yaml`
  - Contains the setup of various self-hosted tools
  - If you have limited memory, you may want to comment out the tools by commenting out the services.

## Starting docker

In this directory, run:

```
docker-compose up
```

## Overview of URL's to use

* Umple
  * http://localhost:8000/umple.php

* Scruffy
  * http://localhost:8080

* Draw.io
  * http://localhost:8081/?offline=1&https=0

## Instructions

* How to use Umple?
  * [Umple syntax](https://cruise.umple.org/umple/GettingStarted.html)
* How to use Scruffy?
  * [Scruffy syntax](https://github.com/aivarsk/scruffy/blob/master/README.rst)
* How to use Draw.io?
  * [Draw.io user manual](https://www.diagrams.net/doc/)

## Running PlantUML and AsciiDoc

For PlantUML we have taken a different approach to the tools above.
We have a simpler setup where you would run a bach container and control the generation of diagrams and documents through a `CLI`.

To get access to the `CLI`, simply run the script `start_asciidoc_and_plant_uml.sh`.

E.g.:

```
% ./start_asciidoc_and_plant_uml.sh
WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
bash-5.1#
```

You are now in a bash shell where all the AsciiDoc tools are available to you. 
The directory that you land at (`/documents`) inside the container is mapped to the `asciidoc` directory outside the container. 
To get access to the `CLI`, simply run the script
