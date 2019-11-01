<template>
  <site-template>
    <span slot="menuesquerdo">
      <img
        src="https://www.wsitebrasil.com.br/sig/www/openged/blog/34/000034_5ad4ef1093728_redessociaislogicadigital.jpg"
        class="responsive-img"
      />
    </span>

    <span slot="principal">
      <h2>Perfil</h2>

      <input type="text" placeholder="Nome" v-model="name" />
      <input type="text" placeholder="E-mail" v-model="email" />
      <input type="password" placeholder="Senha" v-model="password" />
      <input type="password" placeholder="Confirme sua Senha" v-model="password_confirmation" />
      <button class="btn" v-on:click="cadastro()">Enviar</button>
      <router-link class="btn orange" to="/login">Já tenho Cadastro</router-link>
    </span>
  </site-template>
</template>

<script>
import SiteTemplate from "@/templates/SiteTemplate";
import axios from "axios";

export default {
  name: "Perfil",
  data() {
    return {
      name: "",
      email: "",
      password: "",
      password_confirmation: ""
    };
  },
  components: {
    SiteTemplate
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
