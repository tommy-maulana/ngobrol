<p align="center">
  <img title='Ngobrol mascot by @eejitlikeme'
       src="https://jam.systems/img/jam.jpg"
       width="300"
       height="300"/>
</p>

# Ngobrol

Ngobrol is an Open Source alternative to Clubhouse, Twitter Spaces and similar audio spaces.

With Ngobrol you can create `Obrolan` which are audio rooms that can be used for panel discussions, Ngobrol sessions, free flowing conversations, debates, theatre plays, musicals and more. The only limit is your imagination.

[https://jam.systems/](https://jam.systems/)

## Features

🙈 no camera video

📬 no direct messages

🪟 no screen sharing

## Host Your Own Server

Hosting your own Ngobrol server is easy.

1. Install docker and docker-compose (eg. `apt install docker.io docker-compose`)
2. `git clone https://gitlab.com/jam-systems/jam.git`
3. `cd jam/deployment`
4. `cp .env.example .env`
5. `nano .env` set `JAM_HOST` to your domain
6. In your DNS settings point `${JAM_HOST}`, and `*.${JAM_HOST}` to your IP address (if you don't want a wildcard you need the subdomains `pantry`, `signalhub`, `stun` and `turn`)
7. `docker-compose up -d`

## Develop

In in the `ui` directory use `yarn` to install dependencies and `yarn start` to start the local development server.

Directory overview:

`deployment`/ docker compose file for deploying and hosting of Jam

`pantry`/ a lightweight server for handling authentication and coordination of Jam

`signalhub`/ a simple server for managing WebRTC connections for Jam

`ui`/ web based user interface based on the React framework
