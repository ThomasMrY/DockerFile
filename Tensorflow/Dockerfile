FROM tensorflow/tensorflow:1.15.2-gpu-py3-jupyter
LABEL maintainer='username'

RUN apt-get update && apt-get install -y \

	graphviz\
	wget\
	vim\
	p7zip-full\
	git

RUN pip --no-cache-dir install \

	keras==2.2.4\
	opencv-python\
	pillow\
	tqdm\
	jupyter_contrib_nbextensions\
	https://github.com/ipython-contrib/jupyter_contrib_nbextensions/tarball/master\
	pydot\
	graphviz\
    keras-lr-multiplier==0.7.0\
    imageio\
    h5py


# EXPOSE 8888

# COPY jupyter_notebook_config.py ../root/.jupyter/

# RUN jupyter nbextensions_configurator enable --user
# RUN jupyter contrib nbextension install --user

