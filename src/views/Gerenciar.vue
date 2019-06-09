<template>
  <div class="ui container box">
    <div v-on:click="getUser" class="ui cards" v-for="user in users" :key="user.id">
      <div class="card">
        <div class="content">
          <div class="header">{{user.name}}</div>
          <div class="meta">{{user.username}}</div>
        </div>
        <div class="ui buttons">
          <!---->
          <router-link to="manageuser">
            <button :id="user.id" class="ui button">Editar</button>
          </router-link>
          <!--  -->
          <button :id="user.id" class="ui button" v-on:click="deleteUser">Excluir</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import { mapMutations } from "vuex";

export default {
  data() {
    return {
      users: []
    };
  },
  mounted() {
    axios.get("https://jsonplaceholder.typicode.com/users").then(res => {
      this.users = res.data;
      console.log("usuários: ", this.users);
    });
  },
  methods: {
    deleteUser(event) {
      console.log(event.target.id);
      // colocar uma função axios para acessar a rota de exclusão da API
    },
    ...mapMutations(["setSelectedUser"]),
    getUser(event) {
      console.log(event.target.id);
      this.setSelectedUser(this.users[event.target.id - 1]);
      console.log(this.users[event.target.id - 1]);
    }
  }
};
</script>

<style>
.ui.cards {
  display: grid;
}
</style>


