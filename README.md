# sz-jupyter

# TL;DR

Learn Senzing API.
- Run: `docker run -it -p 8888:8888 --rm --name jupyter roncewind/sz-jupyter`
- Open link (cmd-click on mac)

# Intro (TODO)

- Senzing library
- Purpose
- Examples vs tutorials?

## Tutorial list (TODO)

should probably put in the tutorial sub-dir

What story am I telling?

- Fraud detection?
- ???

- Tutorial 1 - add a record
- Tutorial 2 - add a datasource
- Tutorial 3 - add truthset
- Tutorial ...
- Tutorial M - senzing config topics
- Tutorial N - build non-jupyter image and run
- Tutorial N+1 - connect to non-SQLite database
- Tutorial N+2 - deploy tutorial image with docker compose stack
- Tutorial N+3 - deploy tutorial image with cloudformation
- Tutorial N+4 - other deployment topics?

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

# Versioning

A small note about versioning.  The releases of this repo are versioned following
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).  The caveat is that
the release follow Senzing versioning for major and minor with patch versions
specific to this repo.  The rationale being that the tutorials and examples herein
should work on any patch level of the major and minor versions of Senzing.

# TODO:

- API reference into image
- update links to API reference
- Build switch for java and python?
