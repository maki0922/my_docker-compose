FROM python:3.7.3-slim
ARG root_directory=/srv/docker/python3_exam

# install python3 pip
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    # erase cache to delete image size
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    # upgrade pip
    && pip install --upgrade pip

# Copy Current Items to current in container
COPY . ${root_directory}/

# set current directory
WORKDIR ${root_directory}/
