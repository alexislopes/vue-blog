<template>
<div class="ui equal width form container">
  <div class="fields">
    <div class="field">
      <label>Name</label>
      <input type="text" placeholder="Nome">
    </div>
    <div class="field">
      <label>Email</label>
      <input type="email" placeholder="Email">
    </div>
  </div>
  <div class="fields">
    <div class="field">
      <label>Username</label>
      <input type="text" placeholder="Usuario">
    </div>
    <div class="field">
      <label>Senha</label>
      <input type="password" placeholder="Senha">
    </div>
  </div>
  <div v-on:click="cadastraUser" class="ui submit button">Cadastrar</div>
</div>
</template>

<script>
export default {
    data(){
        return {
            nome: null,
            email: null, 
            senha: null,
            usuario: null
        }
    },
    methods: {
        cadastraUser(event) {
            console.log(event.target)
        }
    }
    
}
</script>
