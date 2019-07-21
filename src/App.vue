<template>
    <div id="app">
        <BusinessCard/>
    </div>
</template>

<script>
    import BusinessCard from './components/BusinessCard.vue'

    export default {
        name: 'app',
        components: {
            BusinessCard
        }
    }
</script>

<style>
    @media screen and (min-width: 680px ) {
        #app {
            margin-top: 60px;
        }
    }
</style>
