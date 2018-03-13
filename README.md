AS docker - NodeJS with ExpressJS
========================
implement Docker into Your NodeJS project


Requirements
---
 * configure Your local [projects enrironment](https://bitbucket.org/as-docker/projects-environment)
 * make sure You have [YAKE](https://yake.amsdard.io/) installed


Install
---
Download package by composer (or git clone to Your `~/Projects` directory)
```
npm i nodejs-as-docker
```

 * ExpressJS mode (default)
```
./node_modules/nodejs-as-docker/setup
```


Install - Full sample
---
create a new project
```
npm install express-generator -g
express --view=pug myapp
cd myapp
npm install
```

install as-docker
```
npm i nodejs-as-docker
./node_modules/nodejs-as-docker/setup
```

run the project
```
yake configure
yake up
```


How it works
---
* below file structure will be installed
```
.
├── README.md
├── docker-compose.yml
├── Yakefile
├── deploy
│   ├── prod
│   │   └── docker-compose.yml
│   └── rancher
│       └── docker-compose.yml
└── docker
    ├── mysql
    │   ├── config.env
    │   └── config.env.dist
    └── webapp
        ├── config.env
        ├── config.env.dist
        └── Dockerfile
```
* Your project directory name will be filled as local domain name and docker image namespace (see `docker-compose.yml`)
* new rules will be added to Your `.gitignore` file: 
  * `/docker/*/*.env` container ENV
 
