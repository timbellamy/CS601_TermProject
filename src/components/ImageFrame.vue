<script>
export default {
  name: "ImageFrame",
  props: [
      'name',
      'imageWidth',
      'imageHeight'
  ],
}
</script>

<template>
  <div class="container">
    <img :src="require(`@/assets/images/${ name }`)" alt="">
  </div>
</template>

<style scoped>
img{
  width: v-bind(imageWidth);
  height: v-bind(imageHeight);
}
</style>