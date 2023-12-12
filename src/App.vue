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
  color: #e0e1dd;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  min-height: 100%;
  min-width: 100%;
  display: flex;
  flex-flow: column wrap;
}
#app-container{
  background-color: #1b263b;
}
#components{
  display: flex;
  justify-content: center;
  margin: auto;
  width: 50%;
  padding-top: 5em;
}
</style>
