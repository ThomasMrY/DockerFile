FROM uodcvip/pytorch:1.0
LABEL maintainer='username'


RUN apt-get update; exit 0 && apt-get install -y \

	graphviz\
	wget\
	vim\
	p7zip-full\
	git

RUN pip --no-cache-dir install \

	opencv-python\
    matplotlib\
	pillow\
	tqdm\
	jupyter_contrib_nbextensions\
	https://github.com/ipython-contrib/jupyter_contrib_nbextensions/tarball/master\
	pydot\
	graphviz\
    imageio\
    h5py

# RUN git clone https://github.com/avivga/lord


# EXPOSE 8888

# COPY jupyter_notebook_config.py ../root/.jupyter/

# RUN jupyter nbextensions_configurator enable --user
# RUN jupyter contrib nbextension install --user
