FROM nvidia/cuda:11.7.1-cudnn8-runtime-ubuntu22.04

# get common tools
RUN apt-get update
RUN apt-get install -y software-properties-common tzdata curl sudo

# set timezone
ENV TZ=Asia/Tokyo 

# get python3.10
RUN add-apt-repository ppa:deadsnakes/ppa
RUN apt-get -y install python3.10 python3.10-distutils

# Install pip and pytorch
RUN curl -sS https://bootstrap.pypa.io/get-pip.py | python3.10
RUN python3.10 -m pip install --upgrade pip
RUN python3.10 -m pip install -U wheel setuptools
RUN python3.10 -m pip install --pre torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/nightly/cu117

# Install format tools
RUN python3.10 -m pip install -U autopep8 flake8 mypy

# add user for vscode
RUN adduser --disabled-password --gecos '' --uid 1000 vscode \
    && gpasswd -a vscode sudo \
    && echo 'vscode ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

# apt and pip cache clean up
RUN apt-get clean \
    && rm -rf /var/lib/apt/lists/* \
    && python3.10 -m pip cache purge
