# RobotComp

How to run Jupyter notebook remotely:

Router setuo:
->Go to router setup

->Set static ip for the desktop that you want to use as server

->Set port forwarding for the above ip address(use TCP/UDP protocol and set port range e.g 8889-9999 for both external and internal port range

->Set dynamic DNS(Domain Name servers

Run python notebook:
->jupyter notebook --no-browser --ip=0.0.0.0 --port=8889

Visit the jupyter notebook
-> use browser to open hostname:8889


==============================================
How to install cuDNN:
Step 0: Install cuda from the standard repositories. (See How can I install CUDA on Ubuntu 16.04?)

Step 1: Register an nvidia developer account and download cudnn here (about 80 MB)

Step 2: Check where your cuda installation is. For the installation from the repository it is /usr/lib/... and /usr/include. Otherwise, it will be /usr/local/cuda/ or /usr/local/cuda-<version>. You can check it with which nvcc or ldconfig -p | grep cuda

Step 3: Copy the files:

$ cd folder/extracted/contents
$ sudo cp -P include/cudnn.h /usr/include
$ sudo cp -P lib64/libcudnn* /usr/lib/x86_64-linux-gnu/
$ sudo chmod a+r /usr/lib/x86_64-linux-gnu/libcudnn*
