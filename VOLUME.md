# VOLUME

* The `VOLUME` command defines **mount points** for the container, allowing you to persist data or **share data between the host and the container**. It enables the container to store data that persists beyond the life of the container.

Example:

```dockerfile
VOLUME ["/app/data"]
```

This creates a volume at `/app/data`. When you run the container, you can **mount a host directory** to this path to share data.

## Summary 

* The **host** is the computer where the container runs.
* A **mount point** is a location in the container where you can access files.
* The `VOLUME` command allows you to keep data that outlasts the container’s life.
* **Mounting** connects a folder from the host to a location in the container, allowing them to share files.
  
