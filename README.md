## Preface

In the industrial world, the conveyor system often have some issues as the followings:  
- Objects on the conveyor to be jammed  
- Objects on the conveyor to be overturned  
(Especially when the machine operator can access to the system)
  
These issues may cause any troubles to the system.  
In usual case, these are solved by detecting the faults using sensors.  
But in this sample project, for the issue of object overturning, I have tried the solution by AI instead of using the sensors.  
This means this project might not be the best option to solve this kind of issue, please not that this project is made for my study on AI (and Python).   
The output of this project is like:  
<img src="https://user-images.githubusercontent.com/74876704/104415233-f8b4ba00-55b4-11eb-8835-d2310c2ed799.gif" width="400">

## Requirements
- Jetson Nano Developer Kit  
- Web camera

## Setup

Add a data directory with the following command in the Jetson Nano terminal you've logged into:  
```
mkdir -p ~/nvdli-data
```
  
Docker container  
```
sudo docker pull 0717148/myssd
  
Note:
This container is based on the contrainer from NVIDIA Deep Learning Institute course Getting Started with AI on Jetson Nano.  
[(NVIDIA Deep Learning Institute)](https://www.nvidia.com/en-us/deep-learning-ai/education/).
```



Run the Docker container with the following command
(before running the Docker, please make sure that the web-camera is installed to the Jetson USB port)
```
sudo docker run --runtime nvidia -it --rm --network host \
    --volume ~/nvdli-data:/nvdli-nano/data \
    --device /dev/video0 \
    0717148/myssd:latest
```

## Logging Into The JupyterLab Server
- Open the link address: e.g. 192.168.55.1:8888
- Enter the password: dlinano

## Train and/or test
- Please follow the <readme.md> which is at where you have logged into JupyterLab


