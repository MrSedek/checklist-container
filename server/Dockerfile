FROM python:3
LABEL author="Sedek"
RUN mkdir -p "../home/server"
WORKDIR /home/repos
RUN git clone https://c44e7712cd425ae5027e8d9be1c5354a2468ec61@github.com/MrSedek/WebCheckList.git
RUN cp -r /home/repos/WebCheckList/* /home/server
# ADD WebCheckList /home/server
WORKDIR /home/server
RUN pip3 install -r requirement.txt
# RUN python3 webCheckList.py -s=172.11.0.2 -p=8500
# RUN python3 webCheckList.py -p=8500
EXPOSE 8500