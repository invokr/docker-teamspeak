Docker Teamspeak
=================

![](https://badge.imagelayers.io/invokr/teamspeak:latest.svg)
![](https://img.shields.io/docker/pulls/invokr/teamspeak.svg)
[![Build Status](https://travis-ci.org/invokr/docker-teamspeak.svg?branch=master)](https://travis-ci.org/invokr/docker-teamspeak)

This containers Dockerfile is loosely based on other Teamspeak containers with the
following advantages:

**Graceful termination**: Keeps that pesky data corruption away from your sqlite databases  
**Single data location**: Everything stateful is kept under /ts, including your uploads and logs

Running the container
----------------------

    docker pull invokr/teamspeak
    docker run -name ts3 -d -p 9987:9987/udp -p 30033:30033 -p 10011:10011 -v ts3data:/ts invokr/teamspeak
