<template>
  <div class="ui container">
    <div class="ui piled segment">
      <h4 class="ui header">{{postagem.title}}</h4>
      <p>{{postagem.body}}</p>
    </div>
    <comment></comment>
    <comment-list></comment-list>
  </div>
</template>

<script>
import { mapState } from "vuex";

import CommentForm from "./CommentForm";
import CommentList from "./CommentList";

export default {
  computed: {
    ...mapState(["selectedPost"])
  },
  mounted() {
    this.postagem = this.selectedPost;
    console.log("veio do vuex: ", this.postagem);
  },
  data() {
    return {
      postagem: null
    };
  },
  components: {
    comment: CommentForm,
    "comment-list": CommentList
  }
};
</script>
