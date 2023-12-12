<script>
import ProjectList from '@/models/projects.json';
import Project from "@/components/Project.vue";
export default {
  name: "My Projects",
  components: { Project },
  data(){
    return{
      projectList: ProjectList,
    }
  }
}
</script>

<template>
  <div>
    <h1>Recent Projects</h1>
    <div class="projects" v-for="prj in projectList">
      <Project
          :name="prj.name"
          :description="prj.description"
          :git="prj.git"
          :site="prj.site"
          :thumbnail="prj.thumbnail"
      />
    </div>
  </div>
</template>

<style scoped>
div{
  display: flex;
  flex-flow: column nowrap;
}
h1{
  text-align: center;
}
.projects{
  margin-top: 50px;
  box-shadow: 1em 1em 1em lightslategrey;
  background-color: #778da9;
}
</style>