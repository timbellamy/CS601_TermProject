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
    <div class="menu">
      <ul class="navbar-links">
        <li class="navbar-item">
          <a @click="ChangePage(markRaw(Home))">Home</a>
        </li>
        <li class="navbar-item">
          <a @click="ChangePage(markRaw(Biography))">About</a>
        </li>
        <li class="navbar-item">
          <a @click="ChangePage(markRaw(Resume))">Resume</a>
        </li>
        <li class="navbar-item">
          <a @click="ChangePage(markRaw(ContactMe))">Contact</a>
        </li>
        <li class="navbar-item">
          <a @click="ChangePage(markRaw(Projects))">Projects</a>
        </li>
      </ul>
    </div>
  </nav>

</template>

<style scoped>
.navbar{
  display: flex;
  justify-content: flex-end;
  align-items: center;
  margin-right: 2em;
}

.navbar-links{
  display: flex;
  list-style-type: none;
  cursor: pointer;
}

.navbar-item a{
  display: inline-block;
  padding: 10px 15px;
  text-decoration: none;
}

.navbar-item a:hover{
  text-decoration: solid underline #778da9 3px;
  margin-top: 4px;
}

</style>