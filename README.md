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

- now use it like "all the props are optional except **value**"
    > + **value** `type: number, default:0`
    > + **initial-value** `type: number, default:0`
    > + **animation-delay** `type: number, default:100`
    > + **letter-animation-delay** `type: number, default:100`
    > + **line-height** `type: number, default:1`
    > + **letter-spacing** `type: number, default:1`
    ```vue
    <bounty :value="1000"
        :initial-value="10"
        :animation-delay="100"
        :letter-animation-delay="100"
        :line-height="1"
        :letter-spacing="1">
    </bounty>
    ```