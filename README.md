# Integrate DCM4CHE with OHIF using docker

DCOM4CHE: a collection of open source applications and utilities for the healthcare enterprise.

Ohif: Viewer is a zero-footprint medical image viewer provided by the Open Health Imaging Foundation (OHIF). It is a configurable and extensible

You must have previously installed **docker**, **docker-compose** and **portainer**  on your machine.

After downloading the docker-compose.yml and .env files, run the commands below.

## dcm4chee

Ininitialize dcm4chee container using docker-compose
```bash
docker-compose -p dcm4chee up -d
```
to stop 
```bash
docker-compose -p dcm4chee stop
```

## Portainer
To download and configure ohif, we will use the portainer interface.

Create ohif volume:

![img 1](./docs/image/img-1.png)

Create ohif container:

![img 2](./docs/image/img-2.png)

In Network ports configuration
click in **_publish a new network port_** and define host to **3000** and container to **80**

![img 2.1](./docs/image/img-2.1.png)

In Advanced container settings, go to **_Volumes_** section. Defines container to __/usr/share/nginx/html/__ and select your __ohif-local__ volume.

![img 2.2](./docs/image/img-2.2.png)