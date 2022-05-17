<template>
    <div>
        <AppHeader />
        <div class="joke-heading-box">
            <h3 class="joke-heading">{{ jokes }}</h3>
            <p class="joke-heading-id">ID: {{ $route.params.id }}</p>
        </div>
        <Footer />
    </div>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            jokes: [],
            ho: 'hello'
        }
    },

    async created() {
        const config = {
            headers: {
                "Accept": "application/json"
            }
        }
        try {
            const res = await axios.get(`https://icanhazdadjoke.com/j/${ this.$route.params.id }`, config);
            
            this.jokes = res.data.joke
        } catch (err) {
            console.log(err);
        }
    },

    head() {
        return {
            title: 'dadjokeslessgoooo',
            meta: [
                {
                    name: 'description',
                    content: 'dadjokes wooohooooo'
                }
            ]
        }
    }
}
</script>

<style>
    .joke-heading-box {
        height: 70vh;
        width: 80vw;
        margin: auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }
    .joke-heading {
        margin-inline: auto;
        text-align: center;
    }
    .joke-heading-id {
        padding-top: 2vw;
        font-weight: 600;
        color: rgb(77, 77, 77);
    }
</style>