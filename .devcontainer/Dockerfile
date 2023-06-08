# Use an Ubuntu base image
FROM ubuntu:latest

# Define metadata 
LABEL maintainer="cedr02@live.com" 
LABEL version="1.0"

# Install required packages
RUN apt-get update && apt-get install -y \
    git \
    make \
    gcc-arm-none-eabi \
    gdb-arm-none-eabi \
    libnewlib-arm-none-eabi \
    stlink-tools \
    openocd \
    && rm -rf /var/lib/apt/lists/*
