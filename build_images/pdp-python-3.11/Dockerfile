FROM python:3.11-slim

RUN apt-get update -y \
    && apt-get install -y git curl zip unzip jq make \
    && curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" \
    && unzip awscliv2.zip \
    && sh ./aws/install \
    && rm -rf ./awscliv2.zip \
    && rm -rf ./aws