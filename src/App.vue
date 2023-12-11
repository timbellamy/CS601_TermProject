<template>
  <nav-bar @pageChange="ChangePage($event)"/>
  <div id="components">
    <component :is="Page"></component>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import Home from "@/views/Home.vue";
import {markRaw} from "vue";

export default {
  name: 'App',
  components: {
    NavBar
  },
  computed:{
    Home(){return Home;}
  },
  data(){
    return{
      Page: markRaw(Home)
    }
  },
  methods:{
    ChangePage(page){
      this.Page = page;
      return page;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  display: flex;
  flex-flow: row nowrap;
  min-height: 100%;
  min-width: 100%;
}
#app-container{
  height: 100%;
  width: 100%;
  background-color: sandybrown;
}
#components{
  width: 60%;
  margin: auto;
  align-self: center;

}
</style>
