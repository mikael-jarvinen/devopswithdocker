FROM ubuntu:20.04

# installing git, curl, wget and node
RUN apt-get update && apt-get install -y git curl wget \
    && curl -sL https://deb.nodesource.com/setup_10.x | bash \
    && apt-get install -y nodejs

# For succesfull isntallation of python3
ENV DEBIAN_FRONTEND noninteractive
# installing python
RUN apt-get update && apt-get install -y software-properties-common \
    && add-apt-repository ppa:deadsnakes/ppa \
    && apt-get update \
    && apt-get install -y python3.6

# installing pip and pipenv
RUN apt-get update && apt-get install -y python3-pip \
    && pip3 install pipenv

# installing .net core sdk
RUN wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb \
    && dpkg -i packages-microsoft-prod.deb \
    && apt-get update && apt-get install -y apt-transport-https \
    && apt-get update && apt-get install -y dotnet-sdk-3.1

CMD ["/bin/bash"]
