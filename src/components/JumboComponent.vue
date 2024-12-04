<script>
</script>

<template>
    <div class="container-fluid gx-0">
        <div class="row gx-0" id="home">
            <div class="col-12 col-sm-6">
                <img src="/imgs/banner-image.png" alt="duck image">
            </div>
            <div id="cta-bg" class="col-12 col-sm-6">
                <div>
                    <img src="/imgs/banner-bg.png" alt="duck background">
                </div>
                <div id="cta-text" class="postion-absolute black-text">
                    <h2 class="text-center fs-1">Rubber Ducks Debuggings</h2>
                    <p class="text-center">Spiegare il codice a una paperella di gomma aiuta i programmatori a chiarire il pensiero e individuare errori nascosti.</p>
                    <a href="" class="text-uppercase">Acquistala subito!</a>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import '../style/general.scss';
// Img Styling
img {
    display: block;
    max-width: 100%;
    height: auto;
    object-fit: cover;
}
// CTA
#cta-bg {
    position: relative;
    z-index: 0;
}
#cta-text {
    position: absolute;
    z-index: 3;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
</style>