<template>
  <div class="contactform-container">
    <form class="contact-form" @submit.prevent="sendEmail">
      <label>Nom</label>
      <input class="input" type="text" name="user_name">
      <label>Email</label>
      <input class="input" type="email" name="user_email">
      <label>Message</label>
      <textarea name="message"></textarea>
      <input type="submit" value="Envoyer">
      <div class="submit">
        <button type="submit" value="Send">Envoyer</button>
      </div>
    </form>
  </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
    mounted() {
    console.log('this project 1', process.env.TEST_TEST)    
  },

  methods: {
    sendEmail: (e) => {
      emailjs.sendForm('service_owxtdwe', 'template_g4x6lr1', e.target, 'user_NaM1stgXQWebtXCjHYdox')
        .then((result) => {
            console.log('SUCCESS!', result.status, result.text);
        }, (error) => {
            console.log('FAILED...', error);
        });
    }
  }
}
</script>

<style lang="scss" scoped>
  .contactform-container {
    // border: 1px solid red;
    margin: 40px 0;
    width: 40vw;
    & .contact-form {
      display: flex;
      flex-direction: column;
      & label {
        margin: 20px 0 5px 20px;
        font-size: 14px;
      }
      & .input {
        height: 38px;
      }
      & textarea, .input{
        border-radius: 20px;
        border: none;
        background-color: #F3E8CE;
        padding: 10px 20px;
      }
      & textarea {
        height: 160px;
      }
      & .submit {
        display: flex;
        justify-content: center;
        & button {
          border: none;
          background-color: inherit;
          border-radius: 20px;
          border: 1px solid $brown;
          width: 80px;
          height: 30px;
          cursor: pointer;
          margin: 20px 0;
          font-family: inherit;
          color: $brown;
        }
      & button:hover {
          color: $pink;
          background-color: $brown;
        }
      }
    }
  }
</style>