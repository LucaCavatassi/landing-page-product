<script>
    import HeaderComponent from '../components/HeaderComponent.vue';
    import FooterComponent from '../components/FooterComponent.vue';
    import JumboComponent from '../components/JumboComponent.vue';
    import FeaturesComponent from '../components/FeaturesComponent.vue';

    export default {
        components: {
            HeaderComponent,
            FooterComponent,
            JumboComponent,
            FeaturesComponent
        },
    }
</script>

<template>
    <HeaderComponent />
    <JumboComponent/>
    <FeaturesComponent/>
    <FooterComponent />
</template>

<style scoped lang="scss">
@import '../style/general.scss';

</style>