<script>
import { Handler } from "@netlify/functions";
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
/*    sendEmail(){
      await fetch(`${process.env.URL}/.netlify/functions/emails/subscribed`, {
        headers: {
          "netlify-emails-secret": process.env.NETLIFY_EMAILS_SECRET as string,
        },
        method: "POST",
        body: JSON.stringify({
          from: requestBody.inviteeEmail,
          to: requestBody.subscriberEmail,
          subject: "You've been subscribed",
          parameters: {
            name: requestBody.subscriberName,
            email: requestBody.subscriberEmail,
          },
        }),
      });

      return {
        statusCode: 200,
        body: JSON.stringify("Subscribe email sent!"),
      };
    }*/
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
form{
  display: flex;
  flex-flow: column nowrap;
  justify-content: center;
  width: 20vw;
}
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
  align-self: flex-end;
  width: 10em;
}
button:hover{
  box-shadow: 1em 1em 1em lightslategrey;
}
</style>