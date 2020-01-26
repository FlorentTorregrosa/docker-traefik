# Docker Traefik

Traefik configuration used for local development.

## Installation

After cloning the project, run the following commands:
```shell script
./install-mkcert.sh
./generate-local-certificate.sh
```

This will install [mkcert](https://github.com/FiloSottile/mkcert) on your computer
and generate a self-signed certificate for `*.docker.localhost` domains. Also mkcert
will install a local CA authority that will recognize the previously generated 
self-signed certificate, and allow it on your system and your browsers. So you
will have to manually accept it.

## Usage

After the installation and on a daily basis, just run the following command:
```shell script
docker-compose up
```

This will give you a Traefik using the certificates.
