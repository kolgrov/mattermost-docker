# Production Docker deployment for Mattermost

This project is a fork of mattermost/mattermost-docker. Additions in this repo is:

- Container for reverse proxy using Nginx. Thanks to https://hub.docker.com/r/jwilder/nginx-proxy
- Container for automatic renewal of TLS certificates using Let's Encrypt. Thanks to https://hub.docker.com/r/jrcs/letsencrypt-nginx-proxy-companion

Note:
- Use a .env-file to substitute configuration values in the docker-compose file.
- Go to upstream projects for full readme/docs

### How to update:

Bring down the stack:

```docker-compose down```

Fetch updates from upstream repository:

```git fetch upstream/master```

Make sure that you are at the applicable local branch (most likely master), and merge the fetched local upstream branch into local master branch:

```git checkout master```
```git merge upstream/master```

Solve any merge conflicts.
Rebuild the app from the dockerfile and spin up the containers:

```docker-compose build```
```docker-compose up -d``` (Drop -d if you would like see debug in terminal)
