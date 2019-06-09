<template>
  <div class="ui container">
    <div class="ui comments" v-for="comment in comments" :key="comment.id">
      <div class="comment">
        <div class="content">
          <a class="author">{{comment.name}}</a>
          <div class="text">{{comment.body}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import { mapState } from "vuex";

export default {
  computed: {
    ...mapState(["selectedPost"])
  },
  data() {
    return {
      comments: [],
      users: []
    };
  },
  mounted() {
    axios.get("https://jsonplaceholder.typicode.com/comments").then(res => {
      let realcomments = [];
      this.comments = res.data;
      console.log("comentários: ", this.comments);
      this.comments.forEach(comment => {
        if (comment.postId === this.selectedPost.id) {
          realcomments.push(comment);
        }
        this.comments = realcomments;
      });
      console.log(this.comments.length);
    });

    axios.get("https://jsonplaceholder.typicode.com/users").then(res => {
      this.users = res.data;
      console.log("usuários: ", this.users);
    });
  },
  methods: {}
};
</script>

