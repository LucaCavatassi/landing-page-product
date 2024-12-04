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
                <div id="cta-text" class="postion-absolute black-text text-center">
                    <h2 class="m-2">Rubber Ducks Debuggings</h2>
                    <p class="m-2">Spiegare il codice a una paperella di gomma aiuta i programmatori a chiarire il pensiero e individuare errori nascosti.</p>
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
    width: 100%;
    height: 100%;
    position: absolute;
    z-index: 999;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
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