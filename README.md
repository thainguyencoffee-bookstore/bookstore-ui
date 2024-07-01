## Instructions

Run the following command to build the project.

```shell
./gradlew buildAngular
```

Then, package it in an NGINX container using the [pack](https://buildpacks.io/docs/tools/pack/) CLI and the Paketo Buildpacks.

```shell
pack build bookstore-ui \
  --buildpack gcr.io/paketo-buildpacks/nginx \
  --builder paketobuildpacks/builder:base \
  -p dist
```