<template>
    <div>
        <!-- div created for logo to make it look cleaner -->
        <div class="logo">
            <img src="https://www.seekpng.com/png/full/140-1402510_twitter-logo-white-twitter-logo-svg.png">
        </div>
        <div class="main">
            <button @click="toggleTweet">Toggle Tweet</button>
            <!-- Made twitter card after what we learned in class and am keeping it for future practice and reference (not using for this assignment) -->
            <!-- <TwitterCard v-for="(tweets, index) in tweets" :key="index" :tweetText="tweets.post" :writer="tweets.creator"
            :dateTweeted="tweets.dateCreated" /> -->
        </div>
        <!-- Class binding! Since there are only two states we care about, it was a simple solution -->
        <!-- There's a function monitoring the state of the button, and I was able to determine which class 
             will display based on that state -->
        <div :class="{ card: isCardStyle, }">
            <section v-for="(post, index) in tweets" :key="index">
                <h2>{{ post.post }}</h2>
                <h4>{{ post.creator }}</h4>
                <p>{{ post.dateCreated }}</p>
            </section>
        </div>

    </div>
</template>

<script>

// import TwitterCard from "@/components/TwitterCard.vue";
export default {
    // components: {
    //     TwitterCard
    // },
    name: "UserTweets",
    data() {
        return {
            isCardStyle: true,
            tweets: [
                {
                    post: "Every clock in my room changed daylight time on its own. It is finally the future.",
                    creator: "Kelly Oxford",
                    dateCreated: "2013-04-23"
                },
                {
                    post: "I like to keep a corner of my classroom as a safe place for crying or tantrums. Now I just have to make a spot for the kids too.",
                    creator: "Kate Deal",
                    dateCreated: "2022-08-18"
                },
                {
                    post: "My toddler is pretending to cook a meal and it involves a lot of screaming and throwing food in a pot. She gets it.",
                    creator: "Caroline Bologna",
                    dateCreated: "2022-11-14"
                },
            ],
        }
    },
    methods: {
        toggleTweet() {
            this.isCardStyle = !this.isCardStyle
        }
    },
    mounted() {
        this.toggleTweet();
    }
}
// }
</script>
<!-- this is the styling of the 'twitter card' when the button is in the state of 'isCardStyle = true' -->
<style scoped>
.card {
    border: 2px solid black;
    width: 80%;
    position: relative;
    display: grid;
    left: 50%;
    transform: translateX(-50%);
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 1em;
    background-color: aliceblue;
    margin-top: 5vh;
    padding: 3em 3em;
}

h2 {
    font-style: italic;

}

h4 {
    font-style: italic;
}

img {
    height: 10vh;
}
</style> -->