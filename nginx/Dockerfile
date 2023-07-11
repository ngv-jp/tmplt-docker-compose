# Copyright (c) 2023 RFull Development
# This source code is managed under the MIT license. See LICENSE in the project root.
FROM nginx:latest

RUN apt update && \
    apt install -y fcgiwrap
COPY ./conf.d/default.conf /etc/nginx/conf.d/default.conf

WORKDIR /usr/local/share/nginx/html
COPY ./html/ .

# Clean up
RUN apt clean && \
    rm -rf /var/lib/apt/lists/*
