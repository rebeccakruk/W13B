<template>
  <div id="app">
    <UserTweets />
    <!-- <CardTweets /> -->

  </div>
</template>

<script>

import UserTweets from "@/components/UserTweets.vue";
// import CardTweets from "@/components/CardTweets.vue";
// import UserTweets from "@/components/UserTweets.vue";
// import UserTweets from "@/components/UserTweets.vue";

export default {
  name: 'App',
  components: {
    UserTweets,
    // CardTweets
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
