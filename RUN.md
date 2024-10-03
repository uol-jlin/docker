# RUN

* The `RUN` command executes commands during the **image build process**. It is commonly used to install packages, update system software, or perform any setup necessary to prepare the image.

Example:

```dockerfile
RUN apt-get update && apt-get install -y some-package
```

This example updates the package manager and installs a package during the image build process.
