<script>
    import HeaderComponent from '../components/HeaderComponent.vue';
    import FooterComponent from '../components/FooterComponent.vue';
    import JumboComponent from '../components/JumboComponent.vue';
    import FeaturesComponent from '../components/FeaturesComponent.vue';
    import ReviewsComponent from '../components/ReviewsComponent.vue';

    export default {
        components: {
            HeaderComponent,
            FooterComponent,
            JumboComponent,
            FeaturesComponent,
            ReviewsComponent
        },
    }
</script>

<template>
    <HeaderComponent />
    <JumboComponent/>
    <FeaturesComponent/>
    <ReviewsComponent/>
    <FooterComponent />
</template>

<style scoped lang="scss">
@import '../style/general.scss';

</style>