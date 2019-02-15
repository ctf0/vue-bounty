<h1 align="center">
    Vue Bounty
    <br>
    <a href="https://www.npmjs.com/package/vue-bounty"><img src="https://img.shields.io/npm/v/vue-bounty.svg?style=for-the-badge" alt="npm" /></a> <a href="https://www.npmjs.com/package/vue-bounty"><img src="https://img.shields.io/npm/dt/vue-bounty.svg?style=for-the-badge" alt="npm" /></a>
</h1>

## Installation

```bash
npm install vue-bounty --save
```

## Usage

- register the component

    ```js
    window.Vue = require('vue')

    Vue.component('Bounty', require('vue-bounty').default)
    ```

- now use it like
    ```html
    <bounty value="1000"
        initial-value="10"
        :animation-delay="100"
        :letter-animation-delay="100"
        :line-height="1"
        :letter-spacing="1"
        class="js-bounty">
    </bounty>
    ```

    |          prop          |      required      |       type      |  default  |
    |------------------------|--------------------|-----------------|-----------|
    | value                  | :white_check_mark: | string / number | 0         |
    | initial-value          | :x:                | string / number | 0         |
    | animation-delay        | :x:                | number          | 100       |
    | letter-animation-delay | :x:                | number          | 100       |
    | line-height            | :x:                | number          | 1         |
    | letter-spacing         | :x:                | number          | 1         |
