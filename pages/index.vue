<template>
  <body>
    <div class="login">
      <barraNav></barraNav>
      <center><h2>Log in</h2></center>
      <b-container>
        <label> <h4>E-mail</h4></label>
        <b-form-input placeholder="mariadasilva.r@gmail.com"></b-form-input>
        <label> <h4>Senha</h4> </label>
        <b-form-input placeholder="Ex: ******"></b-form-input>
        <NuxtLink to="/tela-calendario"
          ><b-button class="botão"> login </b-button></NuxtLink
        >
      </b-container>
    </div>
  </body>
</template>

<script>
import barraNav from '~/components/barraNav.vue'
export default {
  name: 'IndexPage',
  components: { barraNav },
  data() {
    return {}
  },
}
</script>
<style>
body {
  /* background: rgb(255,255,255); */
  background: linear-gradient(
    180deg,
    rgba(255, 255, 255, 1) 0%,
    rgba(204, 255, 164, 1) 35%,
    rgba(159, 214, 117, 1) 100%
  );
  background-repeat: no-repeat;
  height: 120vh;
}

.botão {
  width: 15%;
  right: 20%;
  background-color: #589b23;
  border-color: black;
  border-radius: 40px;
  margin: 0 auto;
  color: rgb(0, 0, 0);
  display: block;
  padding: 10px;
  margin-top: 20px;
}
</style>
