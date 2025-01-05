# Dockerfile Bug: Missing `apt-get clean`

This repository demonstrates a common error in Dockerfiles: forgetting to run `apt-get clean` after installing packages.  This can lead to unnecessarily large image sizes and build failures due to cached packages.

The `Dockerfile` shows the problematic code; it installs Python and dependencies but omits the cleanup step.

The `DockerfileSolution.txt` demonstrates the correct approach, which includes the crucial `apt-get clean` command to remove unnecessary downloaded files.

This example highlights the importance of efficient Dockerfile practices for producing smaller, more efficient images.