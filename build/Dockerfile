FROM ghcr.io/linuxserver/baseimage-ubuntu:bionic

ARG DEBIAN_FRONTEND="noninteractive"

WORKDIR /
RUN apt-get update && \
    apt-get install -y \
        default-jre \
        curl \
        # cron \
        perl-modules \
        unzip && \
    apt-get clean -y 
RUN mkdir /hah && \
    curl -Lo /hah/hah.zip https://repo.e-hentai.org/hath/HentaiAtHome_1.6.1.zip && \
    cd /hah/ && \
    unzip hah.zip && \
    chmod 755 /etc

COPY root/ /

EXPOSE 6969

VOLUME /config
VOLUME /dl

ENTRYPOINT ["/init"]
CMD ["/usr/local/bin/hath"]
