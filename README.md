# Confine: Fine-grained System Call Filtering for Container Attack Surface Reduction

## Introduction

Welcome to the official repository for "Confine: Fine-grained System Call Filtering for Container Attack Surface Reduction". Confine uses static code analysis to inspect the containerized application and all its dependencies, identify the superset of system calls required for the correct operation of the container, and generate both a container-wide and application-specific Seccomp system call policy that can be readily enforced while loading the container and launching the main program. 

Read our detailed [research paper](https://mrostamipoor.github.io/files/confine.pdf) to understand the methodology and the principles guiding the development of Confine.


## Build Instructions
To run Confine, copy all necessary libraries and binaries into the `binaries` folder.
Currently, the Nginx container's binaries and libraries are in this directory.
Additionally, you should install Angr.

Then, run Confine using the command below (for example: `python3 main.py nginx 2.31 /usr/sbin/nginx.bak`):
 ```
  python3 main.py containerName glibcVersion PathtoMainProgram
```
You can view the seccomp profile created by Confine for the Nginx container in the `result` directory as an example.


