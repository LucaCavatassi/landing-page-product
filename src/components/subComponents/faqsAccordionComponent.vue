<script>
export default {
    props: {
        questions: {
            type: Object,
            required: true
        }
    }
}
</script>

<template>
    <div class="m-4">
        <div class="accordion" id="myAccordion">
            <!-- ITEM-->
            <div class="accordion-item" v-for="(question, index) in questions" :key="index">
                <!-- Question -->
                <h2 class="accordion-header" :id="'heading' + index">
                    <button type="button" class="accordion-button collapsed fw-bold" data-bs-toggle="collapse" :data-bs-target="'#collapse' + index" 
                    aria-expanded="false" :aria-controls="'collapse' + index">
                        {{ question.question }}
                    </button>
                </h2>
                <!-- /Question -->

                <!-- Answer -->
                <div :id="'collapse' + index" class="accordion-collapse collapse" :aria-labelledby="'heading' + index" data-bs-parent="#myAccordion">
                    <div class="card-body">
                        <p>{{ question.answer }}</p>
                    </div>
                </div>
                <!-- /Answer -->
            </div>
            <!-- /ITEM-->
        </div>
    </div>
</template>

<style scoped lang="scss">
.accordion-button::after {
    background-image: url("data:image/svg+xml,%3csvg viewBox='0 0 16 16' fill='%23333' xmlns='http://www.w3.org/2000/svg'%3e%3cpath fill-rule='evenodd' d='M8 0a1 1 0 0 1 1 1v6h6a1 1 0 1 1 0 2H9v6a1 1 0 1 1-2 0V9H1a1 1 0 0 1 0-2h6V1a1 1 0 0 1 1-1z' clip-rule='evenodd'/%3e%3c/svg%3e");
    transform: scale(.7) !important;
}

.accordion-button:not(.collapsed)::after {
    background-image: url("data:image/svg+xml,%3csvg viewBox='0 0 16 16' fill='%23333' xmlns='http://www.w3.org/2000/svg'%3e%3cpath fill-rule='evenodd' d='M0 8a1 1 0 0 1 1-1h14a1 1 0 1 1 0 2H1a1 1 0 0 1-1-1z' clip-rule='evenodd'/%3e%3c/svg%3e");
}
</style>