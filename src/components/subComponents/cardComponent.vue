<script>
export default {
    props: {
            review: {
            type: Object, // or the appropriate type of your review data
            required: true
            }
        }
    }
</script>

<template>
    <div class="review-card">
        <p>{{ review.description }}</p>
        <p>{{ review.name }}</p>
        <p>{{ review.date }}</p>
    </div>
</template>

<style>

</style>