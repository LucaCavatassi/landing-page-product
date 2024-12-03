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
    <div class="body-font">
        <JumboComponent/>
    </div>
    <FooterComponent />
</template>

<style scoped lang="scss">
@import '../style/general.scss';

</style>