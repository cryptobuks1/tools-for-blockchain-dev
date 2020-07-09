FROM coingateways/dev-komodo:5000f2a.1
RUN apt-get update && \
    apt-get -y install \
    dialog \
    vim \
    git \
    jq && \
    apt-get -y clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN git clone https://github.com/imylomylo/komodo-in-a-box.git && \
  cd /komodo-in-a-box && \
  git checkout starter-kit
CMD ["/bin/bash"]
