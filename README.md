# Docker image for Scancode-Toolkit 3.x
Docker image for the Scancode-Toolkit

# Getting started
```sh
docker run -it -v `pwd`/coding_project/:/scan beevelop/scancode

# Your should now see the verbose output of the scan
# Lean back at grab a cup of coffee

# The result file will be available as licenses.json
cat licenses.json
```

## About
By default this image scans for info, licenses, copyrights, packages, emails and urls in the `/scan` directory. Use volume mappings ( `-v`) to mount the respective folder. The resulting file will be available as `licenses.json`.

To accelerate the scan, this image uses `N-1` available processors. After the scan, you can use the Scancode Workbench to analyse your licenses. Be aware that depending on the size of your project / dependencies, a scan might take quite some time.
