<script>
import Home from "@/views/Home.vue";
import Biography from "@/views/Biography.vue";
import ContactMe from "@/views/ContactMe.vue";
import Resume from "@/views/Resume.vue";
import Projects from "@/views/MyProjects.vue";
import {markRaw} from "vue";
export default {
  computed: {
    Home() { return Home; },
    Biography() { return Biography; },
    ContactMe(){ return  ContactMe; },
    Resume(){ return Resume; },
    Projects() { return Projects; }
  },

  data(){

  },
  methods:{
    markRaw,
    ChangePage: function (view){
      this.$emit('pageChange', view);
    }
  }
}
</script>

<template>
  <nav class="navbar">
    <img src="@/assets/pexels-nimit-kansagra-4509131.jpg" alt=""/>

    <div class="menu">
      <span class="menu-button">Menu</span>
      <ul class="menu-content">
        <li>
          <a @click="ChangePage(markRaw(Home))">Home</a>
        </li>
        <li>
          <a @click="ChangePage(markRaw(Biography))">About</a>
        </li>
        <li>
          <a @click="ChangePage(markRaw(Resume))">Resume</a>
        </li>
        <li>
          <a @click="ChangePage(markRaw(ContactMe))">Contact</a>
        </li>
        <li>
          <a @click="ChangePage(markRaw(Projects))">Projects</a>
        </li>
      </ul>
    </div>
  </nav>

</template>

<style scoped>
.navbar img{
  width: 10vw;
  height: 10vh;
  align-self: flex-start;
}

.navbar{
  width: 10vw;
  min-height: 100%;
  background: rgba(255, 255, 255, 0.1);
}

.navbar .menu-button{
  display: none;
}

.navbar .menu{
  margin-top: 10vh;
}

.navbar .menu li{
  padding-bottom: 3em;
}

.navbar .menu a{
  font-size: 20px;
  text-decoration: none;
}

.navbar .menu :hover{
}
li{
  list-style-type: none;
}
</style>