<template>
    <nuxt-link :to="'jokes/' + id">
        <div class="joke">
            <p>{{ joke }}</p>
        </div>    
    </nuxt-link>
</template>

<script>
export default {
    name: 'Joke',
    props:[ 'joke', 'id' ]
}
</script>

<style>
    .joke {
        width: 90vw;
        padding: 2vw 1vw;
        border-bottom: 1px solid #ccc;
    }

    .joke:nth-last-child() {
        border-bottom: none;
    }
</style>