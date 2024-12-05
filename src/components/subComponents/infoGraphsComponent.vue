<script>
    export default {
        props: {
            info: {
                type: Object,
                required: true
            }
        }
    }
</script>

<template>
    <div class="text-center">
        <svg class="icon" width="36" height="36" fill="currentColor">
            <use :xlink:href="'#' + info.logo"></use>
        </svg>
        <h5 class="fw-bold">{{ info.title }}</h5>
        <p>{{ info.description }}</p>
    </div>
</template>

<style scoped lang="scss">
    @import '../../style/general.scss';

</style>