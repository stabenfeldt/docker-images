FROM ruby:2.4.1-slim
LABEL maintainer="Henning Mosand Stephansen <henning.mosand.stephansen@shortcut.no>, Martin Stabenfeldt <martin.stabenfeldt@shortcut.no>"


RUN apt-get update && apt-get install -y  \
    ack-grep        \
    build-essential \
    freetds-dev     \
    git             \
    libc6-dev       \
    libgmp-dev      \
    libsqlite3-dev  \
    locales         \
    vim             \
    wget

# Install freetds
RUN wget ftp://ftp.freetds.org/pub/freetds/stable/freetds-1.00.21.tar.gz
RUN tar -xzf freetds-1.00.21.tar.gz
WORKDIR freetds-1.00.21
RUN ./configure --prefix=/usr/local --with-tdsver=7.3
RUN make
RUN make install

