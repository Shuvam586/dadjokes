<template>
    <header class="header">
        <h1 class="title">dadjokeslessgooooo</h1>
        <ul>
            <li><nuxt-link to="/">Home</nuxt-link></li>
            <li><nuxt-link to="/jokes">Jokes</nuxt-link></li>
            <li><nuxt-link to="/about">About</nuxt-link></li>
        </ul>
    </header>    
</template>

<script>
export default {
    name:'AppHeader'
}
</script>

<style>
    * {
        margin: 0;
        padding: 0;
    }
    
    .header {
        display: flex;
        width: 96vw;
        height: 4vw;
        margin: 2vw;
    }
    ul {
        width: 100%;
        list-style: none;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
    }
    a {
        color: inherit;
        text-decoration: none;
    }
</style>
