---
title: Installation
description: How to install litekart grocery ecommerce script
---

> How to install litekart grocery ecommerce script

<div class="Alert Alert--nuxt-green">
COMPATIBILITY NOTE: Litekart requires Node.js > 10.x
</div>

## Softwares Required

Download and install the following softwares

- [NodeJS (Web Server)](https://nodejs.org/en/)
- [Redis (Cache)](https://redis.io/)
- [MongoDB (Database)](https://www.mongodb.com/)
- [Yarn](https://yarnpkg.com/en/docs/install)

OR through terminal (Need [chocolatey](https://chocolatey.org/) for windows)

```bash
# For Windows
choco install nodejs mongodb yarn redis
# OR for linux
sudo apt-get install nodejs mongodb redis yarn
```

## Installation

### Start database

Start mongodb in a separate shell
Run the follwoing commands from an elevated termnial/command prompt. In Windows operating system we can start it by opening the following file.

```bash
C:/Program Files/MongoDB/Server/3.2/bin/mongod.exe
```

### Start cache

Start redis in a separate shell
Run the follwoing commands from an elevated termnial/command prompt. In Windows operating system we can start it by opening the following file.

```bash
C:/Program Files/Redis-x64-3.2.100/redis-server.exe
```

### Start GraphQL API

```bash
cd D:/litekart-grocery/api
npm start
```

### Start Store Front

```bash
cd D:/litekart-grocery/www
npm start
```

### Start Vendor APP

```bash
cd D:/litekart-grocery/vendor
npm start
```

### Start Delivery Panel

```bash
cd D:/litekart-grocery/delivery
npm start
```

### Start Admin Panel

```bash
cd D:/litekart-grocery/admin
npm start
```

<div class="Alert Alert--nuxt-green">
**That's it !!!**

You can now access the webapp and the graphql api

</div>

````GraphQL Server: [http://localhost:7700](http://localhost:7700)

Store Front: [http://localhost:7777](http://localhost:7777)

Vendor Panel: [http://localhost:7776](http://localhost:7776)

Delivery Panel: [http://localhost:7775](http://localhost:7775)

Admin Panel: [http://localhost:7774](http://localhost:7774)```

````
