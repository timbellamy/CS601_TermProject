<script>
import ContactForm from '@/components/ContactForm.vue';
import GitLogo from '@/assets/icons/github-mark.svg';
import LinkedInLogo from '@/assets/icons/LI-Logo.png';

export default {
  name: "ContactMe",
  components: {ContactForm},
  data(){
    return{
      GitLogo,
      LinkedInLogo,
    }
  }
}
</script>

<template>
  <div class="contact">
    <h1>Contact Me</h1>
    <contact-form />
    <div class="logo_grp">
      <a href="https://github.com/timbellamy">
        <img class="img_git" :src="GitLogo" alt="" />
      </a>
      <a href="https://www.linkedin.com/in/tim-b-27259969">
        <img class="img_linkedIn" :src="LinkedInLogo" alt="">
      </a>
    </div>
  </div>
</template>

<style scoped>
.contact{
  display: flex;
  flex-flow: column wrap;
  justify-self: center;
  align-self: center;
  justify-items: center;
  align-items: center;
  width: 35vw;
  border: 1px black solid;
  box-shadow: 1em 1em 1em lightslategrey;
  padding: 50px;
  background-color: #778da9;
}
.logo_grp{
  display: flex;
  flex-flow: row wrap;
  justify-content: flex-start;
  align-items: center;
  margin-top: 50px;
}
.img_git{
  width: 50px;
  height: 50px;
}
.img_linkedIn{
  width: 100px;
  margin-left: 25px;
}
</style>