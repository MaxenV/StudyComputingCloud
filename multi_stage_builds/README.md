# What is it

This is a solution to an assignment for the subject "Programming Applications in Cloud Computing" by creating a suitable Dockerfile.

# Dockerfile content

The Dockerfile creates an image based on Scratch and serves an express service on port 8080. <br>
The default page provides information about network, host and version of app.

# Usage

## Download

You can download and run container from [dockerhub](https://hub.docker.com/r/maxenv/multi_stage_builds)
using command:

```
docker run -d -p 8080:8080 maxenv/multi_stage_builds:v1
```

## Build

Alternatively, you can build it on your own using the command:

```
docker build -t maxenv/multi_stage_builds:v1 --build-arg VERSION=v1 --no-cache .
```

then use

```
docker run -d -p 8080:8080 image_name:version
```

to create a container from this image.

# Default page

When your container is running you can check the [default page](http://localhost:8080)
