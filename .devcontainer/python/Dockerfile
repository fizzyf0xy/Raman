FROM python:3.10.13-bookworm

ARG WORKDIR=/workspaces/Raman
WORKDIR ${WORKDIR}

ENV DEBIAN_FRONTEND=noninteractive
# Remove printing buffer to stdout, stderr
# https://stackoverflow.com/questions/59812009/what-is-the-use-of-pythonunbuffered-in-docker-file
ENV PYTHONUNBUFFERED=1
ENV PYTHONPATH=${WORKDIR}
ENV PIPENV_VENV_IN_PROJECT=1

# https://vsupalov.com/docker-arg-env-variable-guide/
# https://bobcares.com/blog/debian_frontendnoninteractive-docker/
ARG DEBIAN_FRONTEND=noninteractive
# Timezone
ENV TZ="Asia/Bangkok"

RUN apt update && apt upgrade -y
# Set timezone
RUN apt install -y tzdata
RUN ln -snf /usr/share/zoneinfo/$CONTAINER_TIMEZONE /etc/localtime && echo $CONTAINER_TIMEZONE > /etc/timezone

# Set locales
# https://leimao.github.io/blog/Docker-Locale/
RUN apt-get install -y locales
RUN sed -i -e 's/# en_US.UTF-8 UTF-8/en_US.UTF-8 UTF-8/' /etc/locale.gen && \
    locale-gen
ENV LC_ALL en_US.UTF-8 
ENV LANG en_US.UTF-8  
ENV LANGUAGE en_US:en  


# error: extension 'gcvspline._gcvspl' has Fortran sources but no Fortran compiler found
RUN apt install -y gfortran

# pipenv
RUN pip install --upgrade pip
RUN pip install pipenv


# # Export Jupyter into PDF
# RUN apt install -y texlive-xetex texlive-fonts-recommended texlive-plain-generic
# RUN apt install -y pandoc

RUN apt clean
RUN rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
CMD sleep infinity