<template>
  <login-template>
    <span slot="menuesquerdo">
      <img
        src="https://www.wsitebrasil.com.br/sig/www/openged/blog/34/000034_5ad4ef1093728_redessociaislogicadigital.jpg"
        class="responsive-img"
      />
    </span>

    <span slot="principal">
      <h2>Cadastro</h2>

        <input type="text" placeholder="Nome" value />
        <input type="text" placeholder="E-mail" value />
        <input type="password" placeholder="Senha" value />
        <input type="password" placeholder="Confirme sua Senha" value />
        <button class="btn">Enviar</button>
        <router-link class="btn orange" to="/login">Já tenho Cadastro</router-link>
    </span>
  </login-template>
</template>

<script>
import LoginTemplate from "@/templates/LoginTemplate";

export default {
  name: "Cadastro",
  data() {
    return {
    };
  },
  components: {
    LoginTemplate
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
