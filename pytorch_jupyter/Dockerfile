FROM pytorch/pytorch:1.3-cuda10.1-cudnn7-devel
LABEL maintainer='username'

RUN apt-get update; exit 0 && apt-get install -y \

	graphviz\
	wget\
	vim\
	p7zip-full\
	git

RUN pip --no-cache-dir install \
	torchvision\
	gin-config\
	tensorboardx\
	opencv-python\
    jupyter\
    matplotlib\
	pillow\
	jupyter_contrib_nbextensions\
	pydot\
	graphviz\
    imageio\
    sklearn\
    tensorflow-gpu==1.15\
    gin-config\
    scipy\
    h5py


RUN apt-get install -y \
	libglib2.0-0 \
	libsm6 \
	libxext6 \
	libxrender-dev \
	libgl1-mesa-dev