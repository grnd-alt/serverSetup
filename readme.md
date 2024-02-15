# ServerSetup hosting everything on belakkaf.net
### this is quite messy and badly documented


## Steps to renew certificate:
* comment out all http to https redirects in nginx
* comment out all ::80 listens
* start the server
	docker compose build
	docker compose up -d
* run
	docker compose run --rm letsencrypt certonly --webroot --webroot-path /var/www/certbot/ -d [domain]
* reset changes


