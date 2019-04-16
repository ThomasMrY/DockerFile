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

RUN apt-get update && \
    apt-get install -y curl bzip2  && \
    curl https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh > /tmp/conda.sh && \
    bash /tmp/conda.sh -b -p /opt/conda && \
    /opt/conda/bin/conda update -n base conda && \
    /opt/conda/bin/conda install faiss-gpu cudatoolkit=9.0 -c pytorch # For CUDA9 && \
    apt-get remove -y --auto-remove curl bzip2 && \
    apt-get clean && \
    rm -fr /tmp/conda.sh

ENV PATH="/opt/conda/bin:${PATH}"



