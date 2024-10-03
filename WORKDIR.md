# WORKDIR

* The `WORKDIR` command sets the working directory for any subsequent `RUN`, `CMD`, `ENTRYPOINT`, `COPY`, or `ADD` commands. It simplifies the Dockerfile by avoiding the need to specify full paths repeatedly.

Example:

```dockerfile
WORKDIR /app
COPY . .
RUN python app.py
```

In this case, all commands after `WORKDIR /app` will be executed in the `/app` directory.

* `WORKDIR /app`: Sets `/app` as the working directory for all following commands.
* `COPY . .`: Copies the current directory's contents (from the **host**) into the `/app` directory in the container.
* `RUN python app.py`: Runs the `app.py` file from the `/app` directory.
