FROM openpai/pai.build.base:hadoop2.7.2-cuda9.0-cudnn7-devel-ubuntu16.04

# install git
RUN apt-get -y update && apt-get -y install git

# install PyTorch dependeces using pip
RUN pip3 --no-cache-dir install torch torchvision

# install visdom dependeces using pip
RUN pip3 install visdom

# install imageio dependeces using pip
RUN pip3 install imageio

# install scipy dependeces using pip
RUN pip3 install scipy

# install sklearn dependeces using pip
RUN pip3 install sklearn

# install skimage dependeces using pip
RUN pip3 install scikit-image

# install numpy dependeces using pip
RUN pip3 install numpy

