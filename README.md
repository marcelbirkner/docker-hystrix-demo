# Hystrix Demo

This repo contains Dockerfiles for running the Netflix Hystrix Dashboard together with the Hystrix Demo app.
To get both docker containers up and running use:

```
docker-compose up
```

To access the dashboard, go to:

- http://192.168.59.103:38080/

To access the demo app, go to:

- http://192.168.59.103:48080/

To generate some traffing, run the following command:

```
while true; do curl "http://192.168.59.103:48080/"; done
```

## Tested on

- MacOS & Boot2Docker

# Dashboard Screenshot

![Hystrix Dashboard of Demo App](https://github.com/marcelbirkner/docker-hystrix-demo/blob/master/screenshots/hystrix-dashboard.png)



