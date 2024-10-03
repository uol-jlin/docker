# ARG

* The `ARG` command defines **build-time variables** that can be passed to the `docker build` command. These variables are not available in the running container but can influence the build process.

Example:

```dockerfile
ARG VERSION=latest
RUN curl -o software-$VERSION.tar.gz https://example.com/software-$VERSION.tar.gz
```

This allows you to specify a different version of the software when building the image.
