<script>
import q from '../assets/quotes.json'
export default {
    data() {
        return {
            quote: null
        }
    },
    methods: {
        changeQuote() {
            let index = Math.floor(Math.random() * q.quotes.length);

            let chosen = q.quotes[index];
            // console.log(q, chosen);
            this.quote = chosen;
        },
    },
    mounted() {
        // alert("mounted");
        this.changeQuote();
        // let index = Math.floor(Math.random() * q.quotes.length);

        // let chosen = q.quotes[index];
        // console.log(q, chosen);
        // this.quote = chosen;
    }

}
</script>

<template>
    <h1 id="quote" v-if="quote != null">
        {{ quote }}
    </h1>
    <a href="#" @click="changeQuote">Neu</a>
</template>

<style>
#quote {
    /* border: 1px solid black; */
}
</style>