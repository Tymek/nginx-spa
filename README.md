# Docker image for Single Page Application on NGINX server

Intended to run behind other service in production. For example Traefik, Caddy, HAProxy or another NGINX as edge reverse proxy router with SSL.

- Port: `80`
- Root: `/srv`

## Features
Please, take a minute to read before using.
- From `nginx:alpine` image
- Redirect `404` and other errors to `/index.html`
- Removed version from `Server` header
- Denied access to hidden files (starting with `.`)
- Enabled and configured `gzip` compression
- Brotli support for precompressed files

## Sources and detailed guides:
- [Vue-CLI Deployment Guide for Docker-NGINX](https://github.com/vuejs/vue-cli/blob/8db62376a5cabe128ac37297988e16a70d883da4/docs/guide/deployment.md#docker-nginx) by [cregetycreg](https://github.com/cregetycreg)
- [How to Add the gzip Module to Nginx](https://www.digitalocean.com/community/tutorials/how-to-add-the-gzip-module-to-nginx-on-ubuntu-14-04) by [Mateusz Papiernik](https://maticomp.net/)
- [Poor man’s Brotli: serve Brotli compressed files without a nginx module](https://siipo.la/blog/poor-mans-brotli-serving-brotli-files-without-nginx-brotli-module) by [Johannes Siipola](https://siipo.la/)
