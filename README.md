# Confine
For runing Confine, you should copy all needed libraries and binaries into `binaries` folder.
Right now, there are Nginx container's binaries and libraries in this directory.
Also, you should install Angr.

Then, run Confine using below command (for example:`python3 main.py nginx 2.31 /usr/sbin/nginx.bak` ):
 ```
  python3 main.py containerName glibcVersion PathtoMainProgram
```
You can see the created seccomp profile by `Confine` for Nginx conatiner in `result` directory as a sample.
Read our detailed [research paper](https://mrostamipoor.github.io/files/confine.pdf) to understand the methodology and the principles guiding the development of Confine.
