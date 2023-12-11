<script>
export default {
  name: "ContactForm",
  data(){
    return{
      name: "",
      email: "",
      message: ""
    }
  },
  methods:{
    sendEmail(){

    }
  }
}
</script>

<template>
  <form>
    <div class="form-input">
      <label for="userName">Name</label>
      <input id="userName" name="userName" type="text" required>
    </div>
    <div class="form-input">
      <label for="email">Email</label>
      <input id="email" name="email" type="email" required>
    </div>
    <div class="form-input">
      <label for="message">Message</label>
      <textarea id="message" name="message" rows="10" cols="50"></textarea>
    </div>
    <button>Send</button>
  </form>
</template>

<style scoped>
.form-input{
  display: flex;
  flex-flow: column nowrap;
  align-content: flex-start;
  justify-content: flex-start;
  text-align: left;
}
button{
  margin-top: 25px;
  padding: 10px;
  background-color: lightskyblue;
  transition: box-shadow .4s;
}
button:hover{
  box-shadow: 1em 1em 1em lightslategrey;
}
</style>