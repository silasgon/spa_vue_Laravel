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

        <input type="text" placeholder="Nome" v-model="name" />
        <input type="text" placeholder="E-mail" v-model="email" />
        <input type="password" placeholder="Senha" v-model="password" />
        <input type="password" placeholder="Confirme sua Senha" v-model="password_confirmation" />
        <button class="btn" v-on:click="cadastro()">Enviar</button>
        <router-link class="btn orange" to="/login">Já tenho Cadastro</router-link>
    </span>
  </login-template>
</template>

<script>
import LoginTemplate from "@/templates/LoginTemplate";
import axios from "axios";

export default {
  name: "Cadastro",
  data() {
    return {
      name:'',
      email: '',
      password:'',
      password_confirmation:''
    }
  },
  components: {
    LoginTemplate
  },
  methods: {
    cadastro() {
      console.log("OK");

      axios
        .post(`http://127.0.0.1:8000/api/cadastro`, {
          name: this.name,
          email: this.email,
          password: this.password,
          password_confirmation: this.password_confirmation
        })
        .then(response => {
          console.log(response)
          if (response.data.token) {
            //login com sucesso
            console.log('Cadastro realizado com sucesso')
            sessionStorage.setItem('usuario', JSON.stringify(response.data));
            this.$router.push('/');
          }else if (response.data.status == false) {
            //login não existe
            alert('Erro no cadastro! tente novamente mais tarde.');
          }else{
            console.log('erros de validação')

            let erros = '';

            for(let erro of Object.values(response.data)){
              erros += erro +" ";
            }
            alert(erros);
          }
        })
        .catch(e => { 
          console.log(e)
          alert("Erro! Tente novamente mais tarde.")
        });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
