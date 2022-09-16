# sz-jupyter

# TL;DR

Learn Senzing API.
- Run: `docker run -it -p 8888:8888 --rm --name jupyter roncewind/sz-jupyter`
- Open link (cmd-click on mac)

# Intro

- Purpose
- Tutorial 1 - add a record
- Tutorial 2 - add a datasource
- Tutorial 3 - add truthset
-

## Run with local directory mounted

Any changes made in a container exists only as long as the container is running.
In order for changes to survive stopping and re-running the docker image, they
must be saved to the host.  To do this mount a directory into the container when
it is run.

Map the current directory into the Docker container so that changes to notebooks are
saved locally.

`docker run -it -p 8888:8888 --rm --name jupyter -v $(pwd):/home/jovyan/work roncewind/sz-jupyter`

This mounts the current directory as the `work` directory in the container.  Any
files saved into that directory will be saved outside the container and therefore
not lost when the container is brought down.


# TODO:

- Build tutorial list/story?
- API reference into image
- update links to API reference
- Build switch for java and python?
