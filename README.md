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
