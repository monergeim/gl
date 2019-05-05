Short Description: This is interactive metrics script which use psutil - cross-platform library for retrieving information on running processes and system utilization.

Full Description: #Where to get help: the Docker Community Forums, the Docker Community Slack, https://pypi.org/help/, https://www.python.org/about/help/ or Stack Overflow

#Where to file issues: https://github.com/monergeim/metrics/issues

#Maintained by: Git repository owner

#Supported architectures: amd64, arm32v5, arm32v6, arm32v7, arm64v8, i386, ppc64le, s390x, windows-amd64

#What is metrics script: Based on python and psutil open library

#Prerequisites:
On host should be installed:
- docker
- wget
- git 2.10 or upper

We have 2 options for preparations to use

1. Check required apps, download metrics bash script, build image from git-hub
whereis docker wget
git --version
wget https://raw.githubusercontent.com/monergeim/gl/master/metrics
chmod u+x metrics
docker build github.com/monergeim/gl -t monergeim/py-mon

2. Check required apps, download metrics bash script, pull created image from docker-hub
whereis docker wget
wget https://raw.githubusercontent.com/monergeim/gl/master/metrics
chmod u+x metrics
docker pull monergeim/py-mon

#How to use this script: ./metrics [-h] arg

positional arguments: arg enter argument mem or cpu to see details

optional arguments: -h, --help show this help message and exit

The script require mandatory single argument to specify which metrics need to print:

cpu - prints CPU metrics
mem - prints RAM metrics

e.g. ./metrics cpu  #if you need to check cpu info

#License: GPL

#Docker image: https://cloud.docker.com/u/monergeim/repository/docker/monergeim/py-mon
