# Note that there must be a tag
FROM pangeo/pangeo-notebook:2019.04.19

# https://mybinder.readthedocs.io/en/latest/tutorials/dockerfile.html#preparing-your-dockerfile
ENV NB_USER jovyan
ENV NB_UID 1000
ENV HOME /home/${NB_USER}

COPY . ${HOME}
USER root
RUN chown -R ${NB_UID} ${HOME}
USER ${NB_USER}

# is this the best way to do this?
RUN pip install git+https://github.com/rabernat/xbatcher.git
