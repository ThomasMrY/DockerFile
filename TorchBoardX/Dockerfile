FROM pytorch/pytorch:1.5.1-cuda10.1-cudnn7-devel
RUN apt-get update \
&& pip --no-cache-dir install scipy \
&& apt-get clean \
&& rm -rf /var/lib/apt/lists/*

RUN pip --no-cache-dir install \

	tensorboardX

# EXPOSE 8888

# COPY jupyter_notebook_config.py ../root/.jupyter/

# RUN jupyter nbextensions_configurator enable --user
# RUN jupyter contrib nbextension install --user

