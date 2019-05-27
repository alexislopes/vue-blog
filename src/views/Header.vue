<template>
    <div class="ui secondary  menu">
  <a class="active item">
    Home
  </a>
  <a class="item">
    Messages
  </a>
  <a class="item">
    Friends
  </a>
  <div class="right menu">
    <div class="item">
      <div class="ui icon input">
        <input type="text" placeholder="Search...">
        <i class="search link icon"></i>
      </div>
    </div>
    <a class="ui item">
      Logout
    </a>
  </div>
</div>
</template>

<style scoped>
    .navbar {
        margin-top: 1em;
        margin-bottom: 1em;
        background-color: indianred
    }

    a {
        text-decoration: none;
        color: aliceblue;
    }

    .navbar-nav a {
        margin-top: .2em
    }
</style>

<script>
export default {
    data() {
        
    }
}
</script>


