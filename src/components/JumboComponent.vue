<script>
</script>

<template>
    <div class="container-fluid gx-0">
        <div class="row gx-0" id="home">
            <div class="col-12 col-sm-6">
                <img src="/imgs/banner-image.png" alt="duck image">
            </div>
            <div class="col-12 col-sm-6">
                <div id="cta-text" class="black-text text-center mt-2 p-4">
                    <h2 class="mt-2 fw-bold">Rubber Ducks Debuggings</h2>
                    <p class="mt-2">Spiegare il codice a una paperella di gomma aiuta i programmatori a chiarire il pensiero e individuare errori nascosti.</p>
                    <div class="mt-5">
                        <a href="" class="text-uppercase mt-3 p-3">Acquistala subito!</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import '../style/general.scss';

@media (min-width: 560px) {
    .row {
        height: 50vh;
        overflow: hidden;
    }
}

.col-12 {
    height: 100%;
    background-image: url(imgs/banner-bg.png);
    aspect-ratio: 1;
    background-size: cover; // Ensure the image covers the entire element
    background-position: center; // Center the image
    background-repeat: no-repeat; // Prevent repeating the image
}

// Img Styling
img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
}
// CTA
#cta-text {
    width: 100%;
    height: 100%;
    h2 {
        font-size: 3rem;
    }
    a {
        color: inherit;
        text-decoration: none;
        cursor: pointer;
        border: 1px solid $black;
    }
    a:hover {
        color: $white;
        background-color: $black;
    }
}

</style>