<template>
  <div id="app">
    <div class="elevator-button" ref="elevatorup">
      <svg class="sweet-svg" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" x="0px" y="0px" viewBox="0 0 100 100" enable-background="new 0 0 100 100" xml:space="preserve" height="100px" width="100px">
        <path d="M70,47.5H30c-1.4,0-2.5,1.1-2.5,2.5v40c0,1.4,1.1,2.5,2.5,2.5h40c1.4,0,2.5-1.1,2.5-2.5V50C72.5,48.6,71.4,47.5,70,47.5z   M47.5,87.5h-5v-25h5V87.5z M57.5,87.5h-5v-25h5V87.5z M67.5,87.5h-5V60c0-1.4-1.1-2.5-2.5-2.5H40c-1.4,0-2.5,1.1-2.5,2.5v27.5h-5  v-35h35V87.5z"></path>
        <path d="M50,42.5c1.4,0,2.5-1.1,2.5-2.5V16l5.7,5.7c0.5,0.5,1.1,0.7,1.8,0.7s1.3-0.2,1.8-0.7c1-1,1-2.6,0-3.5l-10-10  c-1-1-2.6-1-3.5,0l-10,10c-1,1-1,2.6,0,3.5c1,1,2.6,1,3.5,0l5.7-5.7v24C47.5,41.4,48.6,42.5,50,42.5z"></path>
      </svg>
      {{word}}
    </div>
  </div>
</template>

<script>
import ElevatorUp from 'elevator.js'
export default {
  props: {
    word: {
      type: String,
      required: false,
      default: 'Go to Top',
    },
    duration: {
      type: Number,
      required: false,
      default: 4000,
    },
    mainAudio: {
      type: String,
      required: false,
      default: 'http://tholman.com/elevator.js/music/elevator.mp3',
    },
    endAudio: {
      type: String,
      required: false,
      default: 'http://tholman.com/elevator.js/music/ding.mp3',
    },
  },
  data () {
    return {
      elevator: null,
    }
  },
  mounted () {
    this.elevatorUp()
  },
  methods: {
    elevatorUp () {
      // console.log(this);
      this.elevator = new ElevatorUp({
        element: this.$refs.elevatorup,
        duration: this.duration,
        // targetElement: document.querySelector('#elevator-target'),
        // verticalPadding: 100,  // in pixels
        mainAudio: this.mainAudio,
        endAudio: this.endAudio,
      })
      // this.elevator.elevate();
    },
  },
}
</script>

<style>
.elevator-button svg {
  width: 40px;
  height: 40px;
  display: block;
  margin: auto;
  margin-bottom: 5px;
  cursor: pointer;
}
</style>
