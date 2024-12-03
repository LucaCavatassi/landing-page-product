<script>
</script>

<template>
    <div class="grey-bg d-flex justify-content-center">
        <div class="ms-container body-font">
            <h2 class="mb-0 text-center font-size-big p-4 fw-bold black-text">Iscriviti per rimanere aggiornato</h2>
            <p class="fs-6 text-center">Iscriviti alla nostra newsletter per rimanere aggiornato su sconti e novità</p>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import '../style/general.scss';

// Grey Background
.grey-bg {
    background-color: $grey;
}

// Black Text
.black-text {
    color: $black;
}

.ms-container {
    max-width: 540px;
    width: 100%;
    padding: 0 15px;
    box-sizing: border-box; 
}

.font-size-big {
    font-size: 2.5rem;
    overflow-wrap: break-word;
}

@media (min-width: 540px) {
    .font-size-big {
        font-size: 3rem;
    }
}
</style>