# Spotify to Gigs webapp

A Node.js app using [Express 4](http://expressjs.com/).
It allows a user to login into his spotify account, will load the (public) playlists and enable that user to load
the artists from their playlists and check when the artists from that playlist are playing live.

## Running Locally

Make sure you have [Node.js](http://nodejs.org/)

```sh
$ git clone git@github.com:PetitSamuel/playlistToGigs.git # or clone your own fork
$ cd playlistToGigs
$ npm install
$ npm start
```

## with docker

Simply run the following commands:
```sh
$ git clone git@github.com:PetitSamuel/playlistToGigs.git # or clone your own fork
$ cd playlistToGigs
$ git checkout dockerized
$ npm install
$ docker-compose up
```

Your app should now be running on [localhost:5000](http://localhost:5000/).

## Setting up the Spotify API:

You will need to create a spotify application in order to get a client id

```
https://developer.spotify.com/dashboard/login
```

Once you have a client id, add that to :

```
var client_id = 'ADD_CLIENT_ID'; // Your client id
```

You will then want to click on that application and add a redirect uri, for developpement add:
```
http://localhost:5000
```

## Setting up the TicketMaster API:

Create a ticket master developper account and get the client API key that you are given, then add it to the line:
(https://developer.ticketmaster.com/)
```
var key = 'apikey=YOUR_API_KEY' // replace to
var key = 'apikey=abc123'
```
