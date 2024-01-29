FROM debian:12


RUN apt-get update
RUN apt-get install -y python3 python3-pip

WORKDIR /app

COPY . /app

RUN pip install -r requirements.txt --break-system-packages


EXPOSE 5000
