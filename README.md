# About

Just graphhopper router with docker for convenience. API can be reached via nginx reverse proxy (requires basic auth).

Features:

* Routing service using GraphHopper

## Quickstart

Start everything using compose:

```bash
docker-compose up
```

Test if anything meaningful is returned: <http://localhost:1000/info>.

## API

Documentation for graphhopper is available here:
<https://github.com/graphhopper/graphhopper>

## URLs

The following endpoints are available.

Via reverse proxy with password protection:

* <http://localhost:1000/route> - request route
* <http://localhost:1000/info> - check router capabilities

Without reverse proxy:

* <http://localhost:8989/route> - request route
* <http://localhost:8989/info> - check router capabilities
* <http://localhost:8989/maps/> - graphhopper map

## Map data

Map data can be obtained from geofabrik: <http://download.geofabrik.de>.

```bash
wget http://download.geofabrik.de/europe/germany/berlin-latest.osm.pbf
```

## Configuration

Update config.yml. Make sure that the datasource matches the one you provide.

## Credentials

Password is configured in nginx/.htpasswd.

* User: user
* Password: secret

You can use **htpasswd** to change it.

Install it via apt:

```bash
sudo apt-get install apache2-utils
```

Use it:

```bash
htpasswd nginx/.htpasswd <new-user-name>
```
