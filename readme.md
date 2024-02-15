# ServerSetup hosting everything on belakkaf.net
### this is quite messy and badly documented


## Steps to renew certificate:
* comment out all http to https redirects in nginx
* comment out all ::80 listens
* start the server<br>
```
	docker compose build<br>
	docker compose up -d<br>
```
* run<br>
```
	docker compose run --rm letsencrypt certonly --webroot --webroot-path /var/www/certbot/ -d [domain]<br>
```
* reset changes


