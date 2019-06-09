<template>
  <div class="ui items container">
    <div v-on:click="getPostagem" class="item" v-for="post in postagens" :key="post.id">
      <div class="image">
        <!-- <img :src="post.imagem"> -->
      </div>
      <div class="content">
        <router-link class="header" to="postdisplay">
          <a :id="post.id">{{post.title}}</a>
        </router-link>
        <div class="meta">
          <span>{{post.body}}</span>
        </div>
        <div class="description">
          <p></p>
        </div>
        <!-- <div class="extra">{{post.autor}}</div> -->
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import { mapMutations } from "vuex";
import { mapState } from "vuex";

export default {
  computed: {
    ...mapState(["selectedPost"])
  },
  mounted() {
    axios.get("https://jsonplaceholder.typicode.com/posts").then(res => {
      console.log(res.data);
      this.postagens = res.data;
      console.log("postagens: ", this.postagens);
    });
  },
  data() {
    return {
      postagens: {}
    };
  },
  methods: {
    ...mapMutations(["setPostagem"]),
    getPostagem(event) {
      console.log(this.postagens[event.target.id - 1]);
      this.setPostagem(this.postagens[event.target.id - 1]);
      console.log("postagem selecionada através do vuex: ", this.selectedPost);
    }
  }
};
</script>

<style>
.header {
  color: lightslategray;
}
</style>


