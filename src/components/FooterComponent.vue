<script>
</script>

<template>
    <div class="grey-bg d-flex justify-content-center">
        <div class="ms-container body-font">
            <h2 class="mb-0 text-center font-size-big px-4 px-md-5 py-3 fw-bold black-text">Iscriviti per rimanere aggiornato</h2>
            <p class="fs-6 text-center">Iscriviti alla nostra newsletter per rimanere aggiornato su sconti e novità</p>
            
            <form class="mb-5 d-flex align-items-center" action="">
                <input class="ps-0 w-100 form-control" type="email" placeholder="Lascia la tua email qui..." aria-label="Email Input Newsletter">
                <button id="newsletter-btn" type="submit">
                    <!-- SVG symbol provided by Designer -->
                    <svg class="icon" width="36" height="36" fill="currentColor">
                        <use xlink:href="#send"></use>
                    </svg>
                </button>
            </form>
        </div>
    </div>
</template>

<style scoped lang="scss">
@import '../style/general.scss';

// COMMON 
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

// FORM
form {
    position: relative;
}
.form-control {
    background-color: $grey;
    border-bottom: 1px solid grey!important;
    border-top: none;
    border-left: none;
    border-right: none;
    border-radius: 0px;
}

.form-control:focus {
    color: $black;
    background-color: $grey;
    border-color: $green;
    outline: 0;
    box-shadow: 0 0.3rem 0.3rem -0.25rem $green;
}

// Submit Button
#newsletter-btn {
    position: absolute;
    right: 0;
    background: none;
    border: none;
    padding: 0;
    cursor: pointer;

    svg.icon {
        fill: $green!important;
        transition: transform 0.2s ease-in-out;
    }

    &:hover svg.icon {
        transform: scale(1.1); // Slight zoom on hover
    }
}
</style>