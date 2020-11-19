FROM ubuntu:20.10
LABEL author="Sedek"
ENV TZ=Europe/Minsk
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt-get update
RUN apt-get install git -yqq
RUN apt-get install mc -yqq
RUN apt-get install bash
RUN apt-get install iputils-ping -yqq
RUN apt-get install curl -yqq
RUN apt-get install nodejs -yqq
RUN apt-get install npm -yqq
RUN mkdir -p "../home/client"
WORKDIR /home/repos
RUN git clone https://c44e7712cd425ae5027e8d9be1c5354a2468ec61@github.com/MrSedek/react-checklist.git
RUN cp -r /home/repos/react-checklist/* /home/client
WORKDIR /home/client
RUN npm install --no-optional --no-shrinkwrap --no-package-lock
EXPOSE 3000