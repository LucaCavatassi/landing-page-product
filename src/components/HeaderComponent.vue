<script>
</script>

<template>
    <nav class="navbar navbar-expand-md" aria-label="Navbar">
        <div class="container-fluid header-font">
            <!-- Logo -->
            <a class="navbar-brand me-auto" href="#"><img src="../../public/imgs/logo.png" alt="Logo"></a>
            <!-- /Logo -->

            <!-- Toggler Hamburger -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbars"
                aria-controls="navbars" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <!-- /Toggler Hamburger -->

            <!-- Menu -->
            <div class="collapse navbar-collapse" id="navbars">
                <!-- Logo + Close Button -->
                <div class="d-flex d-md-none justify-content-between mt-2">
                    <img src="../../public/imgs/logo.png" alt="Logo">
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbars"
                        aria-controls="navbars" aria-expanded="false" aria-label="Toggle navigation">
                        <font-awesome-icon icon="close" />
                    </button>
                </div>
                <!-- Logo + Close Button -->

                <!-- NavBar -->
                <ul class="navbar-nav ms-auto mb-2 mb-md-0 custom-nav">
                    <li class="nav-item">
                        <a class="nav-link active" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">I punti di forza</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Recensioni</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Paperelle</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">FAQs</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Newsletter</a>
                    </li>
                </ul>
                <!-- NavBar -->
            </div>
            <!-- /Menu -->
        </div>
    </nav>
</template>

<style scoped lang="scss">
@import '../style/general.scss';

// Height Closed
nav {
    max-height: 96px;
    position: relative;
}

// Navbar Style Expanded
.navbar-collapse.show {
    height: 100vh; // Full height when expanded
    width: 70%; // Width applied with smooth transition
    padding-left: 1rem;
    .navbar-nav {
        margin-top: 1rem;
    }
    .nav-item {
        padding-bottom: 0.6rem;
    }
}

// Navbar Style Closed
.navbar-collapse {
    background-color: white !important;
    width: 0;
    position: absolute;
    top: 0;
    right: 0;
    z-index: 3;
    transition: width 0.5s ease-in-out; /* Smooth transition on width */
}

/* Overlay to back content when has show class so it's expanded */
.navbar:has(.navbar-collapse.show)::after {
    content: '';
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 2;
}
// Active link color
.nav-link.active {
    color: $blue!important;
    font-weight: bold!important;
}
// No border on button for open/close
.navbar-toggler {
    border: none!important;
}
// No focus effect on button for open/close
.navbar-toggler:focus {
    box-shadow: none!important;
}

</style>
