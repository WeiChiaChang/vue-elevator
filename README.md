# vue-elevator

[![vue2](https://img.shields.io/badge/vue-2.x-brightgreen.svg)](https://vuejs.org/)

A wrapper of [elevator.js](https://github.com/tholman/elevator.js) in Vue

<p align="center">
  <a target="_blank" href="https://github.com/WeiChiaChang/vue-elevator">
    <img alt="vue2-github-corners" src="https://i.imgur.com/Jra7sKq.gif">
  </a>
</p>

## Demo

[Show me the code, or demo it](https://weichiachang.github.io/vue-elevator/dist/)

## Installation

```
npm i elevator.js
npm i --save vue-elevator
```

## Usage

For standalone version

```javascript
<script src="/dist/vue-elevator.browser.js"></script>
```

For vue-cli user

```javascript
import { VueElevator } from 'vue-elevator'

Vue.component('VueElevator', VueElevator)

```

## Sample

```javascript
<template>
  <div id="app">
    <VueElevator :word="word" :duration="duration" :mainAudio="mainAudio" :endAudio="endAudio"></VueElevator>
  </div>
</template>

export default {
  ...
  data () {
    return {
      // Replace word, duration, mainAudio and endAudio setting as you want.
      // If default is what you like, just don't use related key-value pair and ignore it.
      word: "Go to Top",
      duration: 4000,
      mainAudio: "http://tholman.com/elevator.js/music/elevator.mp3",
      endAudio: "http://tholman.com/elevator.js/music/ding.mp3",
    }
  }
}
```

---

## License

[MIT](http://opensource.org/licenses/MIT) © [WeiChiaChang](https://github.com/WeiChiaChang)
