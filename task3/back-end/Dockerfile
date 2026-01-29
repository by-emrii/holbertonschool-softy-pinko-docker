# Base image
FROM ubuntu:latest

# update and upgrade system packages
RUN apt-get update && apt-get upgrade -y

# install python3 and pip
RUN apt-get install -y python3 python3-pip

# run this before calling pip to fix externally managed env issue
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# install flask using pip3
RUN pip3 install flask

# install flask CORS
RUN pip3 install flask-cors

# set working dir
WORKDIR /app

# copy flask app/python file to docker container
COPY api.py /app/api.py

# fotward the docker container port 5252
EXPOSE 5252

# start flask server
CMD ["python3", "api.py"]