FROM coingateways/zcashparams
RUN apt-get update && \
  apt-get install -y libevent-dev libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev build-essential pkg-config libc6-dev m4 g++-multilib autoconf libtool ncurses-dev python-zmq zlib1g-dev wget curl bsdmainutils automake cmake clang libsodium-dev libcurl4-gnutls-dev libssl-dev git unzip python jq htop

RUN mkdir /opt/komodo
WORKDIR /opt/komodo

RUN git clone https://github.com/mixa84/komodo.git && \
  cd komodo && \
  git checkout cc_mixed && \
  ./zcutil/build.sh -j4 

RUN touch /opt/komodo/komodo.conf

CMD ["/opt/komodo/komodo/src/komodod",  "-regtest=1", "-datadir=/opt/komodo", "-ac_name=TESTCHAIN", "-rpcuser=mylo", "-rpcpassword=mylo", "-rpcallowip=127.0.0.1", "-rpcbind=0.0.0.0", "-rpcallowip=172.17.0.0/16", "-rpcport=17777"]
