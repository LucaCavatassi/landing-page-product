<script>
    import HeaderComponent from '../components/HeaderComponent.vue';
    import FooterComponent from '../components/FooterComponent.vue';
    import JumboComponent from '../components/JumboComponent.vue';


    export default {
        components: {
            HeaderComponent,
            FooterComponent,
            JumboComponent
        },
    }
</script>

<template>
    <HeaderComponent />
    <JumboComponent/>
    <FooterComponent />
</template>

<style scoped lang="scss">
@import '../style/general.scss';

</style>