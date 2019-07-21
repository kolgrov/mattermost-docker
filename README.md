# Production Docker deployment for Mattermost

This project is a fork of mattermost/mattermost-docker. Additions in this repo is:

- Container for reverse proxy using Nginx. Thanks to https://hub.docker.com/r/jwilder/nginx-proxy
- Container for automatic renewal of TLS certificates using Let's Encrypt. Thanks to https://hub.docker.com/r/jrcs/letsencrypt-nginx-proxy-companion

Note:
- Use a .env-file to substitute configuration values in the docker-compose file.
- Go to upstream projects for full readme/docs
