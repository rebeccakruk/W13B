<template>
    <div>
        <!-- NOT USING FOR THIS ASSIGNMENT, BUT KEEPING FOR FUTURE REFERENCE AND PRACTICE -->
        <!-- THERE IS NO STYLING HERE -->
        <h3>{{ tweetText }}</h3>
        <h4>{{ writer }}</h4>
        <p>{{ dateTweeted }}</p>
    </div>
</template>

<script>
export default {
    name: "TwitterCard",
    props: {
        tweetText: String,
        writer: String,
        dateTweeted: String
    }

}
</script>

<style scoped>
div {
    border: 2px solid black;
}
</style>