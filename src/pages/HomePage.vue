<script>
    import HeaderComponent from '../components/HeaderComponent.vue';
    import FooterComponent from '../components/FooterComponent.vue';

    export default {
        components: {
            HeaderComponent,
            FooterComponent
        },
    }
</script>

<template>
    <HeaderComponent />
    <div class="body-font bg-dark">
        <h1>CENTRAL</h1>
    </div>
    <FooterComponent />
</template>

<style scoped lang="scss">

</style>