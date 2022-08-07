FROM debian:testing-slim

RUN apt update && apt upgrade -y \
        && apt install -y golang-1.19
RUN apt install nodejs -y
RUN apt install git -y
RUN mkdir -p /opt/app
WORKDIR /opt/app
RUN git clone https://github.com/DonFynn/evcc.git
WORKDIR /opt/app/evcc
RUN apt install make -y
ENV PATH="/usr/lib/go-1.19/bin:${PATH}"
RUN make && ./evcc
