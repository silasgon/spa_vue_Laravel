 <template>
  <span>
    <header>
      <nav-bar logo="Social" url="#" cor="green darken-1" />
    </header>

    <main>
      <container>
        <router-view />
      </container>
    </main>

    <footer-vue cor="green darken-1" logo="Social" descricao="Teste de descrição" ano="2019">
      <li>
        <a class="grey-text text-lighten-3" href="#!">Home</a>
      </li>
      <li>
        <a class="grey-text text-lighten-3" href="#!">Link 2</a>
      </li>
      <li>
        <a class="grey-text text-lighten-3" href="#!">Link 3</a>
      </li>
      <li>
        <a class="grey-text text-lighten-3" href="#!">Link 4</a>
      </li>
    </footer-vue>
  </span>
</template>

<script>
import NavBar from "@/components/layouts/NavBar";
import FooterVue from "@/components/layouts/FooterVue";

export default {
  name: "App",
  components: {
    NavBar,
    FooterVue
  }
};
</script>

<style>
</style>
