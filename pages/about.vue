<template>
    <div>
        <AppHeader />
        <section class="page">
            <h1>about dadjokes</h1>
            <p>this is an app to tell you dadjokes</p>
            <Person />
            <Footer />
        </section>
    </div>
</template>

<script>
export default {
    head() {
        return {
            title: 'about dadjokeslessgoooo',
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
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

    * {
        margin: 0;
        padding: 0;
    }

    body{
        font-family: 'Poppins', sans-serif;
    }
    
    body::-webkit-scrollbar {
        display: none;
    }

    body {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }
</style>