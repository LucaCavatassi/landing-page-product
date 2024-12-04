<script>
export default {
    props: {
            review: {
            type: Object,
            required: true
            }
        }
    }
</script>

<template>
    <div class="review-card">
        <!-- Review -->
        <p class="r-height">"{{ review.description }}"</p>
        <!-- /Review -->

        <!-- Stars -->
        <div class="my-2">
            <font-awesome-icon class="text-warning" icon="star" />
            <font-awesome-icon class="text-warning" icon="star" />
            <font-awesome-icon class="text-warning" icon="star" />
            <font-awesome-icon class="text-warning" icon="star" />
            <font-awesome-icon class="text-warning" icon="star" />
        </div>
        <!-- /Stars -->

        <!-- Name + Date -->
        <p class="fw-bold mb-4">{{ review.name }} - {{ review.date }}</p>
        <!-- /Name + Date -->
    </div>
</template>

<style>
    .r-height{
        min-height: 119px;
    }
</style>