# HEALTHCHECK

* This command defines a health check for the container, allowing Docker to **monitor the status of the service running inside**. If the service is not healthy, Docker can take actions such as restarting the container.

Example:

```dockerfile
HEALTHCHECK --interval=30s --timeout=10s --retries=3 CMD curl -f http://localhost:8080 || exit 1
```

This health check runs every 30 seconds and uses `curl` to check if the service is responsive. If the command fails (non-zero exit code), Docker will mark the container as unhealthy.
