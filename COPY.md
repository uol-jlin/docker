# COPY

This command is used to **copy files or directories** from the local filesystem into the container's filesystem. It does not handle URLs or archives.

# ADD

Similar to `COPY`, but it can also download files from URLs and extract `.tar` files automatically.

Example:

```dockerfile
COPY . /app           # Copies all files from the current directory to /app in the container
ADD https://example.com/file.tar.gz /app  # Downloads and extracts the tar.gz file to /app
```

In the second case, `ADD` will download the file from teh URL and extract it if it is a compressed archive.
