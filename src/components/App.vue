<template>
  <div id="count-timer">
    <navbar></navbar>
    <h1>Welcome to my website</h1>
    <h2>My time to build this website:</h2>
    <h3>Days: {{ days }} Hours: {{ hours }} Minutes: {{ minutes }} Seconds: {{ seconds }}</h3>
  </div>
</template>

<script>
/* eslint-disable */
import { setInterval } from 'timers';
import Navbar from './Header/Navbar.vue';

export default {
  name: 'App',
  components:{
    Navbar,
  },
data() {
    return {
      timer: null,
      days: null,
      hours: null,
      minutes: null,
      seconds: null,
    };
  },
  created() {
    this.calcTimer();
  },
  methods:{
    calcTimer: function(){
      var self = this;
      setInterval(function(){
        // var date = new Date();
        // if (navigator.userAgent.toLowerCase().indexOf('firefox') > -1) {
        //   self.timer = date.toLocaleTimeString('pt-BR');
        // } else {
        //   self.timer = date.toLocaleTimeString('pt-BR', {timeZone: 'America/Belem'});
        // }
        var data = 'Aug 10, 2019 00:00:00';
        console.log(data);
        var second = 1000,
        minute = second * 60,
        hour = minute * 60,
        day = hour * 24;
        //week = hour * 168;


        var s = new Date(data).getTime(),
        x = setInterval(function() {

          var present = new Date().getTime(),
          gap = s - present;

          self.days =  Math.floor(gap / (day)),
          self.hours = ' ' + Math.floor((gap % (day)) / (hour)),
          self.minutes = ' ' + Math.floor((gap % (hour)) / (minute)),
          self.seconds = ' ' + Math.floor((gap % (minute)) / second);


        });

        var present = new Date().getTime(),
        gap = s - present;
        // if ( Math.floor(gap / (day) < 2 ) ) {
        //   $('#remaining-days-title').text('dia');
        // }

      }, 1000);
    }
  }
}
</script>

<style>
  #count-timer{
    text-align: center;
  }
  ::selection{
    color: cornflowerblue;
  }
</style>