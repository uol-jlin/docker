# CMD

* The `CMD` command specifies the default command to run when a container is started. If no arguments are provided at runtime, `CMD` will execute. If arguments are provided, they will override the default behavior.
* When used with `ENTRYPOINT`, `CMD` can provide default arguments to the executable defined in `ENTRYPOINT`.

Example:

```dockerfile
CMD ["app.py"]
```

If you run the container like this:

```bash
docker run myimage --help
```

If will override `app.py`, running `python --help` instead.
