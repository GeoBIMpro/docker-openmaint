# docker-openmaint
A fully functional openMAINT docker image with docker-compose for integrating with Postgres, BIMServer and GeoServer

## Run using Docker Compose

`docker-compose up`

After that a BIMServer will be available at [http://localhost:8890/bimserver/](), a GeoServer will be available at [http://localhost:8889/geoserver/]() and openMAINT will be available at [http://localhost:8888/openmaint/]().

Currently you will have to access BIMServer page and run the setup. Also in Geoserver you should configure the `cmdbuild` workspace or whatever name you have chosen on openMAINT

## Configuration

Check [Dockerfile](Dockerfile) for available environment variables, they are pretty much self descriptive.

## Notes

* Java 6 and Tomcat 6 for openMAINT. 
* BIMServer version currently necessary is 1.2 (old),so I created my own at [Docker Hub rsilva4/bimserver](https://hub.docker.com/r/rsilva4/bimserver/)
* Geoserver 2.6.1 from [Docker Hub kartoza/geoserver](https://hub.docker.com/r/kartoza/geoserver/)
* Postgres 9.4 with Postgis 2.1.7 from [Docker Hub kpettijohn/postgis](https://hub.docker.com/r/kpettijohn/postgis/)

## Development notes

If you wish to contribute be sure to run the `tests.bats` after your changes and ensuring that every test passes. Add more tests if necessary. Tests built using [BATS](https://github.com/sstephenson/bats) (Bash Automated Testing System).
