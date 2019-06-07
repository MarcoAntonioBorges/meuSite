<template>
  <div>
    <h1>Hello World - Welcome to my website - {{ timer }}</h1>
  </div>
</template>

<script>
import { setInterval } from 'timers';
/* eslint-disable */
export default {
  name: 'App',
  data() {
    return {
      timer: null,
    };
  },
  created() {
    this.calcTimer();
  },
  methods:{
    calcTimer: function(){
      var self = this;
      setInterval(function(){
        var date = new Date();
        if (navigator.userAgent.toLowerCase().indexOf('firefox') > -1) {
          self.timer = date.toLocaleTimeString('pt-BR');
        } else {
          self.timer = date.toLocaleTimeString('pt-BR', {timeZone: 'America/Belem'});
        }
      }, 1000);
    }
  }
}
</script>

<style>

</style>