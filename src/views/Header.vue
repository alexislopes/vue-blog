<template>
  <div class="ui secondary menu container">
    <router-link to="/">
      <a class="item">Home</a>
    </router-link>
    <router-link to="escrever">
      <a class="item">Escrever</a>
    </router-link>
    <router-link to="gerenciar">
      <a class="item">Gerenciar</a>
    </router-link>
    <div class="right menu">
      <div class="item">
        <!-- <div class="ui icon input">
        <input type="text" placeholder="Search...">
        <i class="search link icon"></i>  
        </div>-->
      </div>
      <router-link to="login">
        <a class="ui item">Logout</a>
      </router-link>
    </div>
  </div>
</template>

<style scoped>
</style>

<script>
export default {};
</script>

<style>
</style>



