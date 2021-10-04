<template>
  <main-screen v-if="statusMatch==='defaut'" @onStart="onHandleBeforeStart($event)"/>
  <interact-screen v-if="statusMatch==='match'"/>
</template>

<script>
import MainScreen from './components/MainScreen.vue'
import InteractScreen from './components/InteractScreen.vue'
export default {
  name: "App",
  data(){
    return {
      statusMatch:"defaut",
    }
  },
  components:{
    MainScreen,
    InteractScreen
  },
  methods: {
    onHandleBeforeStart(config){
    console.log("running handle..", config);
    this.statusMatch="match";
    },
  },
};
</script>

<style>
</style>
