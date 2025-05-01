FROM node:20.4

MAINTAINER Hamilton 

RUN npm install -g --unsafe-perm purescript@v0.15.10 spago esbuild

#ENV PURESCRIPT_DOWNLOAD_SHA1 766c6f2945ca92e9ea1a469fe150d964edb67875

#RUN cd /opt \
#    && wget https://github.com/purescript/purescript/releases/download/v0.13.8/linux64.tar.gz \
#    && echo "$PURESCRIPT_DOWNLOAD_SHA1 linux64.tar.gz" | sha1sum -c - \
#    && tar -xvf linux64.tar.gz \
#    && rm /opt/linux64.tar.gz

#ENV PATH /opt/purescript:$PATH 

RUN userdel node

RUN useradd -m -s /bin/bash pureuser 

WORKDIR /home/pureuser

USER pureuser

#RUN mkdir tmp 

#CMD cd tmp && purs repl

CMD spago repl


