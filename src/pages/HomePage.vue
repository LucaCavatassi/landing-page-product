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
    <div class="container">
        <h1 class="body-font">HomePage</h1>
    </div>
    <FooterComponent />
</template>

<style scoped lang="scss">

</style>