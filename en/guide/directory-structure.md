---
title: Directory Structure
description: While architecting the directory structure we took most care towards industry standard, easy to read and modification.
---

> While architecting the directory structure we took most care towards industry standard, easy to read and modification.

## Directories

### The Assets Directory

The `assets` directory contains your un-compiled assets such as Stylus or Sass files, images, or fonts.

### The Components Directory

The `components` directory contains your Vue.js Components.

### The Layouts Directory

The `layouts` directory includes your application layouts. Layouts are used to change the look and feel of your page (for example by including a sidebar).

_This directory cannot be renamed without extra configuration._

### The Middleware Directory

The `middleware` directory contains your Application Middleware. Middleware lets you define custom functions that can be run before rendering either a page or a group of pages (layouts).

### The Pages Directory

The `pages` directory contains your Application Views and Routes. The framework reads all the `.vue` files inside this directory and creates the application router.

_This directory cannot be renamed without extra configuration._

### The Plugins Directory

The `plugins` directory contains your Javascript plugins that you want to run before instantiating the root Vue.js Application. This is the place to register components globally and to inject functions or constants.

### The Static Directory

The `static` directory is directly mapped to the server root (`/static/robots.txt` is accessible under `http://localhost:3000/robots.txt`) and contains files that likely won't be changed (e.g. the favicon)

**Example:** `/static/robots.txt` is mapped as `/robots.txt`

_This directory cannot be renamed without extra configuration._

### The Store Directory

The `store` directory contains your [Vuex Store](http://vuex.vuejs.org/en/) files. The Vuex Store comes with Nuxt.js out of the box but is disabled by default. Creating an `index.js` file in this directory enables the store.

_This directory cannot be renamed without extra configuration._

### The nuxt.config.js File

The `nuxt.config.js` file contains your Nuxt.js custom configuration.

_This file cannot be renamed without extra configuration._

### The package.json File

The `package.json` file contains your Application dependencies and scripts.

_This file cannot be renamed._

<div class="Alert Alert--nuxt-green">

<b>Info:</b> Inside your `vue` templates, if you need to link to your `assets` or `static` directory, use `~/assets/your_image.png` and `~/static/your_image.png`.

</div>
