<template>
  <login-template>
    <span slot="menuesquerdo">
      <img src="https://www.wsitebrasil.com.br/sig/www/openged/blog/34/000034_5ad4ef1093728_redessociaislogicadigital.jpg" class="responsive-img">
    </span>

    <span slot="principal">
      <h2>Login</h2>

      <input type="text" placeholder="E-mail" value />
      <input type="text" placeholder="E-mail" value />
      <button type="button" class="btn">Entrar</button>
    </span>
  </login-template>
</template>

<script>
import LoginTemplate from "@/templates/LoginTemplate";
import CardConteudoVue from "@/components/social/CardconteudoVue";
import CardDetalheVue from "@/components/social/CardDetalheVue";
import PublicarConteudoVue from "@/components/social/PublicarConteudoVue";

export default {
  name: "Login",
  data() {
    return {};
  },
  components: {
    LoginTemplate,
    CardConteudoVue,
    CardDetalheVue,
    PublicarConteudoVue
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
