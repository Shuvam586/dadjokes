<template>
    <div class="main">
        <AppHeader />
        
        <section class="page">
            <h3>this is the best place for dad jokes</h3>
            <PersonTwo />
            <Footer />
        </section>
        
    </div>
</template>

<script>
export default {
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

    .main {
        height: 96vh;
    }

    .page {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-around;
        width: 100vw;
        height: 80vh;
    }
</style>