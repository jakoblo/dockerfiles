# For more information, please refer to https://aka.ms/vscode-docker-python
FROM osgeo/gdal:ubuntu-small-latest

## Language settings
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8

RUN apt-get update --fix-missing
RUN apt-get install -y wget \
	bzip2 \
	ca-certificates \
	build-essential \
	curl \
	git-core \
	pkg-config \
	python3-dev \
	python3-pip \
	python3-setuptools \
	python3-virtualenv \
	unzip \
	software-properties-common \
	llvm

RUN pip3 install --upgrade pip
RUN pip3 install numpy scipy pandas geopandas

# Install Jupyter Lab
RUN pip install jupyter -U && pip3 install jupyterlab
# https://u.group/thinking/how-to-put-jupyter-notebooks-in-a-dockerfile/

WORKDIR /app
COPY . /app

# Creates a non-root user and adds permission to access the /app folder
# For more info, please refer to https://aka.ms/vscode-docker-python-configure-containers
# RUN useradd appuser && chown -R appuser /app
USER root

EXPOSE 8888

CMD ["jupyter", "lab","--ip=0.0.0.0","--allow-root"]
