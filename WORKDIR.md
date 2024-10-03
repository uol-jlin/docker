# WORKDIR

* The `WORKDIR` command sets the working directory for any subsequent `RUN`, `CMD`, `ENTRYPOINT`, `COPY`, or `ADD` commands. It simplifies the Dockerfile by avoiding the need to specify full paths repeatedly.

Example:

```dockerfile
WORKDIR /app
COPY . .
RUN python app.py
```

In this case, all commands after `WORKDIR /app` will be executed in the `/app` directory.
