An e-hentai hentai@home server in the linuxserver fashion

# Install
Copy the default env file to .env
`cp hath.env .env`
Edit .env to reflect your system
`nano .env`
Bring up the container with docker-compose
`docker-compose run lsish-hath`
Answer the ID/key questions to generate the login cert.
# Running
Bring up the container with docker-compose
`docker-compose up lsish-hath`
Alternately bring it up in the background.
`docker-compose up -d lsish-hath`
