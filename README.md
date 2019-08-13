This repo is modified from the Jupyter Notebok Stacks base-notebook.

## What is MMTF?

The Macromolecular Transmission Format (MMTF) is a new compact binary format to transmit and store biomolecular structures for fast 3D visualization and analysis.

## MMTF Addition

This Docker image contains tools needed to run [MMTF](https://github.com/sbl-sdsc/mmtf-pyspark)
(Methods for the parallel and distributed analysis and mining of the Protein Data Bank using MMTF and Apache Spark.)

Originally created as part of the 2018 UCSD Structural Bioinformatics Hackathon - https://github.com/sbl-sdsc/mmtf-workshop-2018

[Methods for mapping genomic data onto 3D protein structure.](https://github.com/sbl-sdsc/mmtf-genomics)  
[Methods for mapping proteomics data on 3D protein structure.](https://github.com/sbl-sdsc/mmtf-proteomics)  

## Using the mmtf-docker Docker image

### Install Docker for your operating systems
[Instructions](https://docs.docker.com/install/) provided by Docker.

### Run Docker image from a directory containing your Jupyter Notebook
```
git clone https://github.com/sbl-sdsc/mmtf-genomics.git
docker run -it --rm -v `pwd`:/home/jovyan/work -p 8888:8888 stevetsa/mmtf-docker
```

### Run Docker image from AWS

Alternatively, you can also run this Docker image from commercial cloud service providers.

From a local machine, [connect to an AWS instance](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AccessingInstancesLinux.html).  

```
### Replace ubuntu@ec2-00-00-000-00.compute-1.amazonaws.com with your AWS Public DNS
ssh -i "/path/to/sshkey.pem" -L 8888:0.0.0.0:8888 ubuntu@ec2-00-00-000-00.compute-1.amazonaws.com
```

From AWS (ubuntu) instance, install docker and run -   

```
### install Docker if needed
sudo apt-get update
sudo apt-get install -y docker.io


### run Docker image from a directory containing your Jupyter Notebook
git clone https://github.com/sbl-sdsc/mmtf-workshop-2018.git
git clone https://github.com/sbl-sdsc/mmtf-genomics.git
docker run -it --rm -v `pwd`:/home/jovyan/work -w `pwd` -p 8888:8888 stevetsa/mmtf-docker

```
Point browser to http://localhost:8888/?token=abc........ (Last line of output from the previous command)

## End of Addition

# Base Jupyter Notebook Stack

Please visit the documentation site for help using and contributing to this image and others.

* [Jupyter Docker Stacks on ReadTheDocs](http://jupyter-docker-stacks.readthedocs.io/en/latest/index.html)
* [Selecting an Image :: Core Stacks :: jupyter/base-notebook](http://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-base-notebook)
