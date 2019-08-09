This repo is modified from the Jupyter Notebok Stacks base-notebook.

## What is MMTF?

The Macromolecular Transmission Format (MMTF) is a new compact binary format to transmit and store biomolecular structures for fast 3D visualization and analysis.

## MMTF Addition

This Docker image contains tools needed to run [MMTF](https://github.com/sbl-sdsc/mmtf-pyspark)
(Methods for the parallel and distributed analysis and mining of the Protein Data Bank using MMTF and Apache Spark.)

Part of the 2018 UCSD Structural Bioinformatics Hackathon - https://github.com/sbl-sdsc/mmtf-workshop-2018

## Run Docker
### Install Docker for your operating systems
[Instructions](https://docs.docker.com/install/) provided by Docker.

### run Docker image from a directory containing your Jupyter Notebook or clone it
git clone https://github.com/sbl-sdsc/mmtf-genomics.git
docker run -it --rm -v `pwd`:/home/jovyan/work -p 8888:8888 stevetsa/mmtf-docker


### Using AWS
From the host, [connect to an AWS instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html)

```
### Replace ubuntu@ec2-00-00-000-00.compute-1.amazonaws.com with your AWS Public DNS
ssh -i "/path/to/sshkey.pem" -L 8888:0.0.0.0:8888 ubuntu@ec2-00-00-000-00.compute-1.amazonaws.com
```

From AWS (ubuntu) instance, install docker and run

```
### install Docker if needed
sudo apt-get update
sudo apt-get install -y docker.io


### run Docker image from a directory containing your Jupyter Notebook or clone it
git clone https://github.com/sbl-sdsc/mmtf-workshop-2018.git
docker run -it --rm -v `pwd`:`pwd` -w `pwd` -p 8888:8888 stevetsa/mmtf-docker

## Open a read-only Jupyter notebook stored in the container
## docker run -it --rm -w /home/jovyan/work -p 8888:8888 stevetsa/mmtf-docker
```

Point browser to http://localhost:8888/?token=abc........ (Last line of output from the previous command)


## End of Addition




[![docker pulls](https://img.shields.io/docker/pulls/jupyter/base-notebook.svg)](https://hub.docker.com/r/jupyter/base-notebook/) [![docker stars](https://img.shields.io/docker/stars/jupyter/base-notebook.svg)](https://hub.docker.com/r/jupyter/base-notebook/) [![image metadata](https://images.microbadger.com/badges/image/jupyter/base-notebook.svg)](https://microbadger.com/images/jupyter/base-notebook "jupyter/base-notebook image metadata")

# Base Jupyter Notebook Stack

Please visit the documentation site for help using and contributing to this image and others.

* [Jupyter Docker Stacks on ReadTheDocs](http://jupyter-docker-stacks.readthedocs.io/en/latest/index.html)
* [Selecting an Image :: Core Stacks :: jupyter/base-notebook](http://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-base-notebook)
