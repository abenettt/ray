---
title: Vue
weight: 8
---


You can send information from Vue (2.x or 3.x) code to Ray via this third party package:

[permafrost-dev/vue-ray](https://github.com/permafrost-dev/vue-ray)

### Installing the package

You can install this third-party package using either `npm` or `yarn`:

```bash
npm install vue-ray

yarn add vue-ray
```

### Installing in Vue 3

When using in a Vue 3.x project, import the package and install the plugin in your entry file:

```js 
import { createApp } from 'vue';
import App from './App.vue';
import RayPlugin from 'vue-ray';

const app = createApp(App);

app.use(RayPlugin, { interceptErrors: true, host: '127.0.0.1', port: 23517 });
```

### Installing in Vue 2

When using in a Vue 2.x project, import the 'vue2' export variant and install the plugin in your entry file:

```js 
const Vue = require('vue');
const { RayPlugin } = require('vue-ray/vue2');

Vue.use(RayPlugin, { interceptErrors: true, host: '127.0.0.1', port: 23517 });
```
