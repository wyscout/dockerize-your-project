# Dockerize your project!

Easy-to-apply instructions for running any project inside a Docker container that use the same environment of the production.

## What?

Following the instructions, any project can be run on the developer's laptop using the same PHP version and PHP extensions.

## Why?

Local development is a great commodity, compared to remote one. In a foreseeable future Sysadmins could make available the docker images really used in production (at the time of writing only the one used by the CI is available), and very different environments could become the norm. Managing that variability from the local machine would be troublesome.

## When?

This kind of dockerization is quite unobtrusive, so it can be applied both in freshly created projects and in older ones. It's just a matter of adding a few files to the project and no further interaction with other systems is required. 

## How?

In this repository are made available a few files to be used as a template; they can be copied to any project and customized at will, because they are just a scaffold. Whilst this solution assumes to serve a Symfony project, with little-to-none editing any project can be run in Docker.

### Installation

The only prerequisite is having installed on the computer both `docker` and `docker-compose`; having that, it's just matter of following these steps:

1. copy the `docker-compose.yml` file and the `docker` directory inside the project
2. edit the files to adapt them to the project's specificities (the files are fully annotated)
3. run `docker-compose up`

### Execution and debugging

PHP is configured to automatically start a remote debugging session connecting to `localhost:9000`; since the containers are run without network isolation the IDE sees the debug session as local, so no registration or specific IDE key has to be defined
