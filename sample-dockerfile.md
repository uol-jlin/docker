```dockerfile
# 1. Specify the base image
FROM python:3.9-slim

# 2. Set environment variables (optional)
ENV PYTHONUNBUFFERED=1

# 3. Set the working directory inside the container
WORKDIR /app

# 4. Copy local files to the container
COPY . /app

# 5. Install required dependencies
RUN pip install --no-cache-dir -r requirements.txt

# 6. Expose a port 
EXPOSE 8080

# 7. ENTRYPOINT - define a fixed executable for the container
ENTRYPOINT ["python"]

# 8. CMD - default arguments passed to the ENTRYPOINT
CMD ["app.py"]

# 9. USER (optional) - set the user the container will run as
RUN useradd -m myuser
USER myuser

# 10. VOLUME (optional) - mount a directory from the host system
VOLUME ["/app/data"]

# 11. HEALTHCHECK - monitor the container's health (optional)
HEALTHCHECK --interval=30s --timeout=10s --retries=3 CMD curl -f http://localhost:8080 || exit 1
```
