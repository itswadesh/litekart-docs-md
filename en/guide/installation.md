---
title: Installation
description: How to install litekart grocery ecommerce script
---

> Installations local/server is free for all. Please let me know if you need any help.

<div class="Alert Alert--nuxt-green">
COMPATIBILITY NOTE: Litekart requires Node.js > 14.x
</div>

## Softwares Required

Download and install the following softwares

- [NodeJS (Web Server)](https://nodejs.org/en/)
- [Redis (Cache)](https://redis.io/)
- [MongoDB (Database)](https://www.mongodb.com/)

OR through terminal (Need [chocolatey](https://chocolatey.org/) for windows)

```bash
# For Windows
choco install nodejs mongodb redis
# OR for linux
sudo apt-get install nodejs mongodb redis
```

## Start database

Start mongodb in a separate shell
Run the follwoing commands from an elevated termnial/command prompt. In Windows operating system we can start it by opening the following file.

```bash
C:/Program Files/MongoDB/Server/3.2/bin/mongod.exe
```

## Start cache

Start redis in a separate shell
Run the follwoing commands from an elevated termnial/command prompt. In Windows operating system we can start it by opening the following file.

```bash
C:/Program Files/Redis-x64-3.2.100/redis-server.exe
```

<div class="Alert Alert--nuxt-green">
Run the following commands in separate shell/terminal/command prompt
</div>

This will install the required node dependencies and start the web apps

## Start GraphQL API

Modify `api/.env` with your credentials and run the following commands

```bash
cd D:/litekart-grocery/api
npm start
```

## Start Applications

```bash
cd D:\litekart-grocery
npx http-server www -p 7777 -P http://localhost:7700
npx http-server vendor -p 7776 -P http://localhost:7700
npx http-server delivery -p 7775 -P http://localhost:7700
npx http-server admin -p 7774 -P http://localhost:7700
```

<div class="Alert Alert--nuxt-green">
**That's it !!!**

You can now access the webapp and the graphql api

</div>

GraphQL Server: [http://localhost:7700](http://localhost:7700)

Store Front: [http://localhost:7777](http://localhost:7777)

Vendor Panel: [http://localhost:7776](http://localhost:7776)

Delivery Panel: [http://localhost:7775](http://localhost:7775)

Admin Panel: [http://localhost:7774](http://localhost:7774)

## Uploading to server

### GraphQL API

You can upload the api part to cloud servers like

[Heroku](https://www.heroku.com/) / [Digital Ocean](https://www.digitalocean.com/) / [Vultr](https://www.vultr.com/)

### Client Apps

This can be uploaded to static hosts based on nodejs [Netlify](https://www.netlify.com/)

- Change `www/netlify.toml`, `vendor/netlify.toml`, `delivery/netlify.toml`, `admin/netlify.toml` to your webserver address
- Copy those folders (www, vendor, delivery, admin) one by one to netlify and you are done.
