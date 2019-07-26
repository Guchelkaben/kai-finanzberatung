<template>
    <div class="page container">
        <div class="page-wrapper">
            <Portrait />
            <Details />
        </div>
    </div>
</template>

<script>
    import Portrait from './portrait/Portrait.vue';
    import Details from './details/Details.vue';

    export default {
        name: 'HelloWorld',
        components: {
            Portrait,
            Details
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
    body {
        background-color: #003366;
        font-family: 'Poppins', sans-serif;
    }

    @media screen and (max-width: 680px ) {
        .container {
            padding: 0;
        }
    }

    @media screen and (min-width: 1000px ) {
        .container {
            padding: 0;
        }

        .page-wrapper {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
        }
    }

    .page {
        flex-wrap: nowrap;
        justify-content: center;
    }

    .page-wrapper {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
</style>
