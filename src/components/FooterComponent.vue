<script>
</script>

<template>
    <footer id="newsletter">
        <!-- Newsletter -->
        <div class="grey-bg d-flex justify-content-center">
            <div class="ms-container body-font">
                <!-- Info Text -->
                <h2 class="mb-0 text-center font-size-big px-4 px-md-5 py-3 fw-bold black-text">Iscriviti per rimanere
                    aggiornato</h2>
                <p class="fs-6 text-center">Iscriviti alla nostra newsletter per rimanere aggiornato su sconti e novità
                </p>
                <!-- /Info Text -->

                <!-- Newsletter Form -->
                <form class="mb-5 d-flex align-items-center" name="contact" method="POST" data-netlify="true">
                    <input class="ps-0 w-100 form-control" type="email" name="email" required
                        placeholder="Lascia la tua email qui..." aria-label="Email Input Newsletter">
                    <button id="newsletter-btn" type="submit">
                        <!-- SVG symbol provided by Designer -->
                        <svg class="icon" width="36" height="36" fill="currentColor">
                            <use xlink:href="#send"></use>
                        </svg>
                    </button>
                </form>
                <!-- /Newsletter Form -->
                <!-- Socials -->
                <div class="ms-socials mb-4 d-flex justify-content-center gap-3">
                    <a target="_blank" href="https://github.com/LucaCavatassi/landing-page-product">
                        <svg class="icon" width="42" height="42" fill="currentColor">
                            <use xlink:href="#facebook"></use>
                        </svg>
                    </a>
                    <a target="_blank" href="https://github.com/LucaCavatassi/landing-page-product">
                        <svg class="icon" width="42" height="42" fill="currentColor">
                            <use xlink:href="#twitter"></use>
                        </svg>
                    </a>
                    <a target="_blank" href="https://github.com/LucaCavatassi/landing-page-product">
                        <svg class="icon" width="42" height="42" fill="currentColor">
                            <use xlink:href="#youtube"></use>
                        </svg>
                    </a>
                    <a target="_blank" href="https://github.com/LucaCavatassi/landing-page-product">
                        <svg class="icon" width="42" height="42" fill="currentColor">
                            <use xlink:href="#linkedin"></use>
                        </svg>
                    </a>
                    <a target="_blank" href="https://github.com/LucaCavatassi/landing-page-product">
                        <svg class="icon" width="42" height="42" fill="currentColor">
                            <use xlink:href="#instagram"></use>
                        </svg>
                    </a>
                </div>
                <!-- /Socials -->
            </div>
        </div>
        <!-- /Newsletter -->

        <!-- Copyright -->
        <div>
            <h6 class="text-center m-3">© 2024 Boolanding Product - Designed by Boolean</h6>
        </div>
        <!-- /Copyright -->
    </footer>
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
    border-bottom: 1px solid lightgray !important;
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
    color: $green;

    .icon {
        transition: transform 0.2s ease-in-out;
    }

    .icon:hover {
        transform: scale(1.1);
    }

}

// Socials
.ms-socials {
    color: $green;

    a {
        color: inherit !important;
    }

    .icon {
        border: 1px solid lightgrey;
        padding: 0.5rem;
        border-radius: 50%;
        transition: transform 0.2s ease-in-out;
    }

    .icon:hover {
        transform: scale(1.1);
        cursor: pointer;
        box-shadow: 0 0.3rem 0.3rem -0.25rem $green;
    }
}

h6 {
    color: $black;
    font-weight: lighter;
}
</style>