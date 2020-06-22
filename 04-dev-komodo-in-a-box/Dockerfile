FROM coingateways/dev-komodo:5000f2a
RUN apt-get update && \
    apt-get -y install \
    dialog \
    git \
    jq && \
    apt-get -y clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN git clone https://github.com/komodo-cakeshop/komodo-in-a-box.git
CMD ["/bin/bash"]
