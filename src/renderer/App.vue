<template>
  <div id="app">
  </div>
</template>

<script>
  import io from 'socket.io-client';
  var played = [];

  export default {
    name: 'inked-lite',
    mounted: function (){
      const socket = io('http://13.209.232.176:3001/client');
      // var socket = io.connect()
      socket.on("alert", function (id) {
        if (played.includes(id)){
          return
        }
        played.push(id)
        var audio = new Audio('http://13.209.232.176:3000/static/sound-effects/tone-1.wav');
        audio.play();

        if (played.lenght > 1000){
          played = [];
        }
      })
    },
    methods: {

    }
  }
</script>

<style>
  /* CSS */
</style>
