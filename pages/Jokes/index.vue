<template>
    <div>
        <AppHeader />
        <div class="joke-box">
            <Joke v-for="joke in jokes" :key="joke.id" :joke='joke.joke' :id="joke.id"/>
        </div>
        <Footer />
    </div>    
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            jokes: []
        }
    },

    async created() {
        const config = {
            headers: {
                "Accept": "application/json"
            }
        }
        try {
            const res = await axios.get('https://icanhazdadjoke.com/search?limit=30', config);
            
            console.log(res)
            this.jokes = res.data.results;
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
    body::-webkit-scrollbar {
        display: none;
    }

    body {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }

    .joke-box {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
</style>