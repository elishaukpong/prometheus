# PROMETHEUS via Docker

This is a simple monitoring setup using prometheus and cadvisor.

Cadvisor is a tool that monitors docker containers and can generate metrics for them.

These metrics is then fed into prometheus and can be monitored from the dashboard.

## Dockerfile

The docker file has 4 services running
    
- Prometheus
- Nginx
- Cadvisor
- Redis

### TO SETUP

- Clone Repo
- copy `.env.example` file to `.env` as it is used by the docker services.
- Check and confirm that needed exposable ports are open, available and accessible on your host machine
- run `docker-composer up -d` and wait for the build to be complete
- open `localhost:${SERVICE_1_PORT}/index.html` on your browser to access the simple html document on the nginx
- open `localhost:${PROMETHEUS_PORT}` on your browser to access the prometheus dashboard
- open `localhost:${CADVISOR_PORT}` on your browser to access the cadvisor dashboard


## Note

Each service has a folder inside the docker folder and contains config where neccessary, 
you can play around with it as you see fit.

### TO BE ADDED

 - Alerts
 - Grafana
 - Rules
 - Percona
