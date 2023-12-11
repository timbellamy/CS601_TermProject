<script>
import ImageFrame from "@/components/ImageFrame.vue";

export default {
  name: "Project",
  components: {ImageFrame},
  props:[
      "name",
      "description",
      "git",
      "site",
      "thumbnail"
  ]
}
</script>

<template>
  <div class="project">
    <h2> {{ name }}</h2>
    <p>{{ description }}</p>
    <div class="links">
      <a :href="site">
        <image-frame :name="thumbnail" :image-height="'125px'" :image-width="'125px'" />
      </a>
      <a :href="git">
        <img class="git_logo"  :src="require('@/assets/icons/github-mark.png')" alt="">
      </a>
    </div>
  </div>
</template>

<style scoped>
.project{
  display: flex;
  flex-flow: column nowrap;
  align-items: center;
  justify-items: center;
  border: 1px solid black;
  padding: 25px;
}
.git_logo{
  width: 100px;
  height: 100px;
  margin-left: 20px;
}
.links{
  display: flex;
  flex-flow: row nowrap;
  align-items: center;
  justify-items: center;
}
</style>