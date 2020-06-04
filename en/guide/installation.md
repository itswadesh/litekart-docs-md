---
title: Installation
description: How to install litekart ecommerce script
---

> How to install litekart ecommerce script

<div class="Alert Alert--nuxt-green">
COMPATIBILITY NOTE: Litekart requires Node.js 10.x
</div>

## Softwares Required

Download and install the following softwares

- [NodeJS (Web Server)](https://nodejs.org/en/)
- [MongoDB (Database)](https://www.mongodb.com/)
- [Yarn](https://yarnpkg.com/en/docs/install)

OR through terminal (Need [chocolatey](https://chocolatey.org/) for windows)

```bash
# For Windows
choco install nodejs mongodb yarn python2
# OR for linux
sudo apt-get install nodejs mongodb yarn python2
```

## Node Gyp

We also need node-gyp installed. Please follow the steps to install it
[https://github.com/nodejs/node-gyp#installation](https://github.com/nodejs/node-gyp#installation)

## Installation

Download and unzip the file from codecanyon and navigate inside the directory

```bash
cd litekart
```

### Start database

Start mongodb in a separate shell
Run the follwoing commands from an elevated termnial/command prompt. In Windows operating system we can start it by opening the following file.

```bash
C:/Program Files/MongoDB/Server/3.2/bin/mongod.exe
```

### Run the following 2 commands

This will install the required node dependencies and start the following

GraphQL Server: [http://localhost:7700](http://localhost:7700)
Store Front: [http://localhost:7777](http://localhost:7777)
Delivery Panel: [http://localhost:7777](http://localhost:7776)
Vendor Panel: [http://localhost:7777](http://localhost:7775)
Admin Panel: [http://localhost:7777](http://localhost:7774)

```bash
cd D:\litekart\litekart-api
yarn
yarn dev
```

```bash
cd D:\litekart\litekart-mono
yarn
yarn dev
```

**That's it !!!**

You can now navigate to the corresponding addresses

## Building files for production server

<img src="./img/deploy.png" alt="deployment"/>

Add your logo/icon(512px\*512px) to static directory of store-front (This step is essential to generate icons for Progressive Web App)

The follwing command will generate both client and server files inside dist directory which can be directly copied to production server

```bash
yarn prod
```

Now copy the files inside **.nuxt** and **dist** directory to the production server (For both store front and store back office)

### Start the server

Login to cloud shell and run the following command

```bash
yarn start
```

<div class="Alert Alert--nuxt-green">

<b>Info:</b> replace <code>&lt;project-name&gt;</nom-du-projet></code> with a name for the project.

</div>
