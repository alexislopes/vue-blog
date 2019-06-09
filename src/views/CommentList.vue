<template>
  <div class="ui comments">
    <div class="comment">
      <div class="content">
        <a class="author">Christian Rocha</a>
        <div
          class="text"
        >I'm very interested in this motherboard. Do you know if it'd work in a Intel LGA775 CPU socket?</div>
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
      this.comments = res.data;
      console.log(this.comments);
    });

    axios.get("https://jsonplaceholder.typicode.com/users").then(res => {
      this.users = res.data;
      console.log(this.users);
    });
  },
  methods: {}
};
</script>

