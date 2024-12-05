<script>
export default {
    props: {
        item: {
            type: Object,
            required: true,
        }
    }
}
</script>

<template>
    <img class="img-fluid" :src="item.img_path" alt="">
    <font-awesome/>
    <p class="fw-semibold fs-4 my-2" >{{ item.name }}</p>
    <p class="fw-bold fs-5 my-2 mb-4">{{ item.price }}$</p>
</template>

<style scoped lang="scss">
    @import '../../style/general.scss';
    p.fw-bold{
        color: $green;
    }
</style>