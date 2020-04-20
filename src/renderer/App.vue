<template>
  <div id="app">
    <button v-on:click="playaudio">play sound</button>
  </div>
</template>

<script>
  export default {
    name: 'inked-lite',
    methods: {
      playaudio: function () {
        var audio = new Audio('http://13.209.232.176:3000/static/sound-effects/tone-1.wav');
        audio.play();
      }
    }
  }
</script>

<style>
  /* CSS */
</style>
