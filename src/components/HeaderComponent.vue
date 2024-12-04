<script>
export default {
    data() {
        return {
            activeSection: '', // Keeps track of the currently active section
        };
    },
    methods: {
        scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                section.scrollIntoView({ behavior: 'smooth' }); // Smooth scroll to section
                this.activeSection = sectionId; // Set the active section
            }
        }
    },
    mounted() {
        const navbarTogglers = document.querySelectorAll('.navbar-toggler'); // Select both togglers
        const navbarCollapse = document.querySelector('.navbar-collapse');
        const navLinks = document.querySelectorAll('.nav-link');

        if (navbarTogglers && navbarCollapse) {
            navbarTogglers.forEach((toggler) => {
                toggler.addEventListener('click', () => {
                    setTimeout(() => {
                        // Check if the navbar is open or closed after Bootstrap transition
                        if (navbarCollapse.classList.contains('show')) {
                            document.body.style.overflow = 'hidden'; // Disable scrolling when open
                        } else {
                            document.body.style.overflow = ''; // Enable scrolling when closed
                        }
                    }, 300); // Delay to sync with Bootstrap's animation timing
                });
            });

            // Close navbar and enable scrolling when a nav link is clicked
            navLinks.forEach((link) => {
                link.addEventListener('click', () => {
                    if (window.innerWidth <= 767) {
                        navbarCollapse.classList.remove('show'); // Close navbar
                        document.body.style.overflow = ''; // Enable scrolling
                    }
                });
            });
        }
    },
    beforeUnmount() {
        // Cleanup event listeners
        const navbarTogglers = document.querySelectorAll('.navbar-toggler');
        const navLinks = document.querySelectorAll('.nav-link');

        if (navbarTogglers) {
            navbarTogglers.forEach((toggler) => {
                toggler.removeEventListener('click', () => {});
            });
        }

        if (navLinks) {
            navLinks.forEach((link) => {
                link.removeEventListener('click', () => {});
            });
        }
    }
};
</script>

<template>
    <nav class="navbar navbar-expand-md sticky-top" aria-label="Navbar">
        <div class="container-fluid header-font">
            <!-- Logo -->
            <a class="navbar-brand me-auto" href="#"><img src="/imgs/logo.png" alt="Logo"></a>
            <!-- /Logo -->

            <!-- Toggler Hamburger -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbars"
                aria-controls="navbars" aria-expanded="false" aria-label="Toggle navigation">
                <!-- SVG symbol provided by Designer -->
                <svg class="icon" width="48" height="48" fill="currentColor">
                    <use xlink:href="#navbar-icon"></use>
                </svg>
            </button>
            <!-- /Toggler Hamburger -->

            <!-- Menu -->
            <div class="collapse navbar-collapse" id="navbars">
                <!-- Logo + Close Button -->
                <div class="d-flex d-md-none justify-content-between mt-2">
                    <img src="../../public/imgs/logo.png" alt="Logo">
                    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbars"
                        aria-controls="navbars" aria-expanded="false" aria-label="Toggle navigation">
                        <font-awesome-icon icon="close" class="fa-lg" />
                    </button>
                </div>
                <!-- Logo + Close Button -->

                <!-- NavBar -->
                <ul class="navbar-nav ms-auto mb-2 mb-md-0 custom-nav">
                    <li class="nav-item">
                        <a :class="{ active: activeSection === 'home' }" @click.prevent="scrollToSection('home')" class="nav-link" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a :class="{ active: activeSection === 'features' }" @click.prevent="scrollToSection('features')" class="nav-link" href="#">I punti di forza</a>
                    </li>
                    <li class="nav-item">
                        <a :class="{ active: activeSection === 'reviews' }" @click.prevent="scrollToSection('reviews')" class="nav-link" href="#">Recensioni</a>
                    </li>
                    <li class="nav-item">
                        <a :class="{ active: activeSection === 'shop' }" @click.prevent="scrollToSection('shop')" class="nav-link" href="#">Paperelle</a>
                    </li>
                    <li class="nav-item">
                        <a :class="{ active: activeSection === 'faqs' }" @click.prevent="scrollToSection('faqs')" class="nav-link" href="#">FAQs</a>
                    </li>
                    <li class="nav-item">
                        <a :class="{ active: activeSection === 'newsletter' }" @click.prevent="scrollToSection('newsletter')" class="nav-link" href="#">Newsletter</a>
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

// Height
nav {
    max-height: 96px;
    position: relative;
    background-color: white !important;
}


// Navbar Style (Mobile default)
.navbar-collapse {
    background-color: white !important;

    width: 0; // Start collapsed
    overflow: hidden;
    transition: width 0.5s ease-in-out !important; // Smooth width transition
    visibility: hidden; // Initially hidden

    // When toggled shows apply 
    &.show {
        position: absolute;
        top: 0;
        right: 0;
        z-index: 3;
        height: 100vh; // Full height when expanded
        width: 70%; // Expanded width
        padding-left: 1rem; // Add padding for menu items
        visibility: visible; // Make visible when expanded
    }
}

// Override Bootstrap collapsing behavior
.navbar-collapse.collapsing {
    height: auto !important; // Disable height transition
    display: block !important; // Ensure visible during transition
    overflow: hidden !important; // Prevent overflow
    transition: none !important; // Disable Bootstrap's default animation
}

// Prevent flicker (mobile-specific)
@media (max-width: 767.98px) {
    .collapse:not(.show) {
        width: 0 !important; // Collapse width
        visibility: hidden !important; // Hide when collapsed
    }

    .collapse.show {
        width: 70% !important; // Expanded width
        visibility: visible !important; // Ensure visibility
    }
}

// Desktop behavior
@media (min-width: 768px) {
    .navbar-collapse {
        overflow: visible !important; // Allow content to flow
        width: auto !important; // Reset width
        height: auto !important; // Reset height
        position: static !important; // Default Bootstrap behavior
        display: flex !important; // Inline menu for desktop
        transition: none !important; // No transitions
        visibility: visible !important; // Always visible
    }

    .collapse:not(.show) {
        display: flex !important; // Always visible
        visibility: visible !important; // Ensure visibility
    }
}

// Overlay for expanded navbar (mobile only)
@media (max-width: 767.98px) {
    .navbar:has(.navbar-collapse.show)::after {
        content: '';
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        background-color: rgba(0, 0, 0, 0.5); // Dark overlay
        z-index: 2;
        opacity: 1; // Fully visible
        transition: opacity 0.5s ease-in-out; // Smooth fade-in
    }

    .navbar:has(.navbar-collapse:not(.show))::after {
        opacity: 0; // Hide overlay
        pointer-events: none; // Prevent interaction
    }
}

// Active link color + weight
.nav-link.active {
    color: $blue !important;
    font-weight: bold !important;
}

// No border on button for open/close
.navbar-toggler {
    border: none !important;
}

// Remove focus styles from toggler
.navbar-toggler:focus {
    box-shadow: none !important;
}
</style>