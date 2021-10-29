# Dockerfile for docker-bottle web application

# Add a base image to build this image off of
FROM ubuntu
RUN apt update -y && apt-get install -y python3 python3-pip python3-dev build-essential
COPY requirements.txt /usr/src/app/
RUN pip3 install -r /usr/src/app/requirements.txt
COPY app.py /usr/src/app/
# Add a default port containers from this image should expose
EXPOSE 8080

# Add a default command for this image
CMD python3 /usr/src/app/app.py
