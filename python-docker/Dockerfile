FROM ubuntu:16.04

MAINTAINER bluecloud0429 bluecloud0429@gmail.com

ENV PATH /usr/local/bin:$PATH
ENV LANG C.UTF-8

RUN apt-get update
RUN apt-get install -y software-properties-common python-software-properties
RUN add-apt-repository -y ppa:jonathonf/python-3.6
RUN apt-get update
RUN apt-get install -y build-essential python3.6 python3.6-dev python3-pip
RUN apt-get install -y git

RUN python3.6 -m pip install pip --upgrade

ADD . /python-docker

EXPOSE 5000

WORKDIR /python-docker

RUN pip3 install -r requirements.txt

CMD python3.6 app.py
