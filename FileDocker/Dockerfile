FROM openpai/pai.build.base:hadoop2.7.2-cuda9.0-cudnn7-devel-ubuntu16.04

# install git
RUN apt-get -y update && apt-get -y install git

RUN apt-get update && \
    apt-get install -y curl bzip2  && \
    curl https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh > /tmp/conda.sh && \
    bash /tmp/conda.sh -b -p /opt/conda && \
    /opt/conda/bin/conda update -n base conda && \
    /opt/conda/bin/conda install faiss-gpu cudatoolkit=9.0 -c pytorch # For CUDA9 && \
    apt-get remove -y --auto-remove curl bzip2 && \
    apt-get clean && \
    rm -fr /tmp/conda.sh

# install PyTorch dependeces using pip
RUN conda install pytorch torchvision cudatoolkit=9.0 -c pytorch


# install visdom dependeces using pip
RUN python3 -m pip install -q visdom

# install imageio dependeces using pip
RUN python3 -m pip install -q imageio

# install scipy dependeces using pip
RUN python3 -m pip install -q scipy

# install sklearn dependeces using pip
RUN python3 -m pip install -q sklearn

# install skimage dependeces using pip
RUN python3 -m pip install -q scikit-image

# install numpy dependeces using pip
RUN python3 -m pip install -q numpy

ENV PATH="/opt/conda/bin:${PATH}"

# install jupyter, matplotlib dependeces using pip
RUN python3 -m pip install -q jupyter matplotlib



