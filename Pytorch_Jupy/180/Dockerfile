FROM pytorch/pytorch:1.8.1-cuda11.1-cudnn8-devel
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
    scikit-learn==0.22.2\
    gin-config\
    scipy\
	lpips\
	natsort\
    h5py


RUN apt-get install -y \
	libglib2.0-0 \
	libsm6 \
	libxext6 \
	libxrender-dev \
	libgl1-mesa-dev
