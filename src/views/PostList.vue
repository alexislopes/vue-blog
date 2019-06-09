<template>
  <div class="ui items container">
    <div class="item" v-for="post in postagens" :key="post.id">
      <div class="image">
        <!-- <img :src="post.imagem"> -->
      </div>
      <div class="content">
        <a class="header">{{post.title}}</a>
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

export default {
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
  methods: {}
};
</script>

