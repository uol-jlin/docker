# ENTRYPOINT

* The `ENTRYPOINT` command defines the main command that is executed when **a container starts**. This command makes the container behave like an executable.
* Unlike `CMD`, which can be overriden, `ENTRYPOINT` will not be replaced by any arguments passed to `docker run`. Instead, those arguments will be appended to the command specified in `ENTRYPOINT`.

Example:

```dockerfile
ENTRYPOINT ["python"]
```

Whenever the container is started, it will run `python`. Additional arguments, such as script names or options will be passed to `python`.

```bash
docker run myimage app.py --verbose
```

This runs `python app.py --verbose`.
