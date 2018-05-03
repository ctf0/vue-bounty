# vue-bounty

[![npm](https://img.shields.io/npm/v/vue-bounty.svg?style=for-the-badge)](https://www.npmjs.com/package/vue-bounty) [![npm](https://img.shields.io/npm/dt/vue-bounty.svg?style=for-the-badge)](https://www.npmjs.com/package/vue-bounty)

## Installation

```bash
npm install vue-bounty --save
```

## Usage

- register the component

    ```js
    window.Vue = require('vue')

    Vue.component('Bounty', require('vue-bounty'))
    ```

- now use it like

    ```vue
    <bounty :value="100"></bounty>
    ```