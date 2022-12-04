<template>
  <div id="app">
    <UserTweets msg="Welcome to Tweetie" />

  </div>
</template>

<script>

import UserTweets from "@/components/UserTweets.vue";


export default {
  name: 'App',
  components: {
    UserTweets,
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

body {
  background-color: #1D9BF0;
}
</style>
