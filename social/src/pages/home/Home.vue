<template>
  <card-conteudo-vue
    perfil="https://materializecss.com/images/yuna.jpg"
    nome="Maria Silva"
    data="08/10/2019 17:10">

    <card-detalhe-vue img="http://archives.materializecss.com/0.100.2/images/sample-1.jpg"
    titulo=""
    txt="I am a very simple card. I am good at containing small bits of information.
              I am convenient because I require little markup to use effectively"
    />
      

  </card-conteudo-vue>
</template>

<script>
import CardConteudoVue from "@/components/social/CardconteudoVue";
import CardDetalheVue from "@/components/social/CardDetalheVue";

export default {
  name: "Home",
  data() {
    return {};
  },
  components: {
    CardConteudoVue,
    CardDetalheVue
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
