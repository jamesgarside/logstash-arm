# Logstash builds for ARM
This repo will contain builds of Kibana for ARM. 

If the build you are looking for isn’t here please contact me.
Feel free to branch and update yourselves. 

## Docker Description
This a modified version of the Official Dockerfile found [here](https://github.com/elastic/dockerfiles/blob/7.10/Logstash/Dockerfile)


## Docker Images
Pre-built docker images can be found on my Dockerhub [here](https://hub.docker.com/r/jamesgarside/Logstash/).

- [Logstash 7.10.0](https://hub.docker.com/r/jamesgarside/Logstash/tags)
- [Logstash 7.9.3](https://hub.docker.com/r/jamesgarside/Logstash/tags)

## Usage
A basic `Docker-coompose.yml` file has been included with is repo to allow for basic testing. It will create one Logstash instance.

### Elastic Stack
I have an Elastic Stack for ARM Repo which can be [found here](https://github.com/jamesgarside/elastic-stack-arm).
This repo will deploy a full 3 node Elasticsearch Cluster with Crypt (TLS) along with a single Kibana Instance by running one script. 

## TODO
- [x] Create basic Dockerfile
- [ ] Package Logstash for Debian/Ubuntu Systems
- [ ] Package Logstash for CentOS/RHEL Systems


## Disclaimer
I've not fully tested these builds and as they are not 'supported' by Elastic I cannot gaurentee there won’t be issues, however in my testing I'm yet to come across any. 

## Changes
### env2yaml
This binary is used for feeding Environment Vars to Logstash. 
It has been recompiled to work with ARM64 which enables Logstash to run as an ARM64 container.

### Dockerfile
Some RUN commmands were added which swap out the packaged JDK version with an ARM64 compatiable version.