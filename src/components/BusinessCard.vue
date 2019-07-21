<template>
    <div class="page container">
        <div class="d-flex justify-content-center">
            <Portrait/>
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
    }

    @media screen and (max-width: 680px ) {
        .container {
            padding: 0;
        }
    }

    .page {
        max-width: 600px;
    }
</style>
