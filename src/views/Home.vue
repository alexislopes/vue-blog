<template>
  <post-list></post-list>
</template>

<script>
import PostList from "./PostList";

export default {
  components: {
    "post-list": PostList
  }
};
</script>

<style scoped>
.item {
  margin-left: 2rem;
}
</style>
