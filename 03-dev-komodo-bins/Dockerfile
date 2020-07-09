FROM ubuntu:18.04
RUN apt-get update && \
    apt-get -y install \
    build-essential \
    pkg-config \
    libc6-dev \
    m4 \
    autoconf \
    libboost-all-dev \
    libsodium-dev \
    curl \
    libtool \
    make \
    ncurses-dev \
    unzip \
    python \
    zlib1g-dev \
    wget \
    bsdmainutils \
    automake \
    libssl-dev \
    libprotobuf-dev \
    protobuf-compiler \
    libqrencode-dev \
    libdb++-dev \
    libcurl4-gnutls-dev \
    libgconf-2-4 && \
    apt-get -y clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
#RUN wget https://github.com/KomodoPlatform/komodo/releases/download/dev-multios-0.4.0a-alpha/linux_0.4.0a.tar.gz
RUN wget https://github.com/KomodoPlatform/komodo/releases/download/cd_release_5000f2a_dev/komodo_5000f2a_dev_linux.zip
RUN unzip komodo_5000f2a_dev_linux.zip && \
 mv komodod /usr/local/bin && \
 mv komodo-cli /usr/local/bin
CMD ["/bin/bash"]
