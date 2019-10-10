<template>
 
  <div class="row">
    <grid-vue tamanho="12" class="input-field">
      <textarea id="textarea1" class="materialize-textarea"></textarea>
      <label for="textarea1">O que está acontecendo?</label>
    </grid-vue>
    <p>
      <grid-vue tamanho="2 offset-s10" class="btn waves-effect waves-ligth">Publicar</grid-vue>
    </p>
  </div>
  
</template>

<script>
import GridVue from "@/components/layouts/GridVue";

export default {
  name: 'PublicarConteudoVue',
  props: [],
  data() {
    return {

    }
  },
  components: {
    GridVue
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
