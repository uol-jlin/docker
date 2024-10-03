# USER

* By default, Docker containers run as the **root user**, which can pose security risks. The `USER` command allows you to switch to a different user for running processes inside the container.
* You typically create a user using the `RUN` command and then switch to that user with `USER`.

Example:

```dockerfile
RUN useradd -m myuser
USER myuser
```

This sets up a new user named `myuser` and switches to it for any subsequent commands.
