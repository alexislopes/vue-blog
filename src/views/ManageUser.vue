<template>
  <div class="ui container">
    <form class="ui form">
      <h4 class="ui dividing header">User's Information</h4>
      <div class="field">
        <label>Name</label>
        <div class="field">
          <input
            :value="user.name"
            type="text"
            name="shipping[first-name]"
            placeholder="First Name"
          >
        </div>
      </div>
      <label>Email</label>

      <div class="field">
        <input
          :value="user.email"
          type="email"
          name="shipping[address]"
          placeholder="Email Address"
        >
      </div>

      <label>Username</label>
      <div class="field">
        <input :value="user.username" type="text" name="shipping[address]" placeholder="Username">
      </div>

      <div class="two fields">
        <div class="field">
          <label>Permissão</label>
          <select class="ui fluid dropdown">
            <option>Permissão</option>
            <option value="CAD">Cadastrado</option>
            <option value="ADM">Admin</option>
          </select>
        </div>
      </div>
      <div class="ui button" tabindex="0" v-on:click="salvarUser">Salvar</div>
    </form>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  mounted() {
    this.user = this.selectedUser;
  },
  computed: {
    ...mapState(["selectedUser"])
  },
  data() {
    return {
      user: null
    };
  },
  methods: {
    salvarUser() {
      //função axios para salvar usuario através da rota na API
    }
  }
};
</script>

