# What
An e-hentai hentai@home server in the linuxserver fashion, with a proper init and the s6 overlay and some basic Perl (for now- it will probably get reimplemented in python soon).

# Why
The goal is to provide a Hentai@Home server container that (eventually) contains tools that can help collectors perform other automated tasks when they use it as a downloader.

# How
## Install

Copy the default env file to .env

`cp hath.env .env`

Edit .env to reflect your system

`nano .env`

Bring up the container with docker-compose to ensure it logs in properly (or roll the dice and skip to the Running section below):

`docker-compose run lsish-hath`

If you filled in your ID and key properly, the service should start up and you should see something like this in the output:

`lsish-hath    | 2021-06-04T19:16:08Z [info] H@H initialization completed successfully. Starting normal operation`

If instead it asks you for your ID and key, answer the ID/key questions to generate the login cert.

Either way, ctrl-c out of the server, then run it in the background.

## Running

Bring up the container with docker-compose

`docker-compose up lsish-hath`

Alternately bring it up in the background.

`docker-compose up -d lsish-hath`
