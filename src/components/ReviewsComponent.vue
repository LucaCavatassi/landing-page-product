<script>
    import cardComponent from './subComponents/cardComponent.vue';

    export default {
        components: {
            cardComponent,
        }
    }
</script>

<template>
    <div id="reviews">
        <div class="container">
            <h2 class="fw-bold text-center">Cosa ne pensano i nostri sviluppatori</h2>
            <cardComponent/>
        </div>
    </div>
</template>

<style>
    h2 {
        font-size: 3rem;
    }

    @media (min-width: 576px) {
        h2 {
            font-size: 2.5rem!important;
        }
    }
</style>