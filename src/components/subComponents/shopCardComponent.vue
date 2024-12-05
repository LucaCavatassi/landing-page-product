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
    <!-- Img -->
    <img class="img-fluid" :src="item.img_path" :alt="item.name + ' img'">
    <!-- /Img -->

    <!-- Stars -->
    <div class="my-2">
            <font-awesome-icon class="text-warning" icon="star" />
            <font-awesome-icon class="text-warning" icon="star" />
            <font-awesome-icon class="text-warning" icon="star" />
            <font-awesome-icon class="text-warning" icon="star" />
            <font-awesome-icon class="text-warning" icon="star" />
    </div>
    <!-- /Stars -->

    <!-- Description -->
    <p class="fw-semibold fs-4 my-2" >{{ item.name }}</p>
    <p class="fw-bold fs-5 my-2 mb-4">{{ item.price }}$</p>
    <!-- /Description -->

</template>

<style scoped lang="scss">
    @import '../../style/general.scss';
    p.fw-bold{
        color: $green;
    }
</style>