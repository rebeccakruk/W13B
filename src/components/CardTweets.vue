<template>
    <div>
        <button @click="ShowTweet" class="toggle">Toggle</button>
        <UserTweets />
    </div>
</template>

<script>
// import UserTweets from '@/components/UserTweets.vue'
export default {
    name: "ButtonHandler",
}



</script>

<style scoped>
div {
    border: black solid 2px;
}
</style>