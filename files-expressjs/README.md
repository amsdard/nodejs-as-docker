{name}
========================
* [local] {name}.test
* [dev] {name}.app.amsdard.io
* [live] 

Requirements
---
 * configure Your local [projects enrironment](https://bitbucket.org/as-docker/projects-environment)
 * make sure You have [YAKE](https://yake.amsdard.io/) installed


Run project
---
```
yake configure
yake up
yake install
```
* make sure `{name}.test` domain is routed to Your localhost


Additional info
---
* do not use `--save-dev` in `npm install` task (keep common vendors)


Deploy (dev / rancher)
---
```
yake deploy webapp
```
* import `./deploy/rancher/docker-compose.yml` into Rancher + complete ENVs
* make sure `mysql` works on specific host (Scheduling)
* make sure `webapp` has *Health Check* enabled


Deploy (prod)
---
```
yake deploy webapp
```
* import `./deploy/prod/docker-compose.yml` into server + copy ENV files from `docker` directory
* `docker-compose pull --parallel --quiet`
* `docker-compose up -d --force-recreate`

