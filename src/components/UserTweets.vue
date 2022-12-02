<template>
    <div>

        <div v-if="CardStyle === true" class="card">
            <H3>{{ tweets }}</H3>
            <h4>{{ creator }}</h4>
            <p>{{ DateCreated }}</p>
        </div>
        <div v-else class="list">
            <H3>{{ tweets }}</H3>
            <h4>{{ creator }}</h4>
            <p>{{ DateCreated }}</p>
        </div>
    </div>
</template>

<script>
// import CardTweets from './CardTweets.vue';

export default {
    name: "UserTweets",
    data() {
        return {
            tweets: ["Every clock in my room changed daylight time on its own. It is finally the future.", "I like to keep a corner of my classroom as a safe place for crying or tantrums. Now I just have to make a spot for the kids too.", "My toddler is pretending to cook a meal and it involves a lot of screaming and throwing food in a pot. She gets it."],
            creator: ["Kelly Oxford", "Kate Deal", "Caroline Bologna"],
            DateCreated: ["2013-04-23", "2022-08-18", "2022-11-14"],
            TwitterCard: true
        }
    },
    methods: {
        // ShowTweet() {
        // if (this.CardStyle === true) {
        // } else {
        //     document.querySelector(`.list`).insertAdjacentHTML(`beforeend`, `<h2>${this.creator}</h2>`)
        // }

    },
    mounted() {
        console.log("toggle");
        // this.ShowTweet();
    }
}
// }
// }
</script>

<style scoped>
.TwitterCard {
    border: 2px solid black;
}
</style>