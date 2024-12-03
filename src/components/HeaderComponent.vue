<script>
</script>

<template>
    <h1>Sono l'Header</h1>

    <nav class="navbar navbar-expand-md" aria-label="Navbar">
        <div class="container header-font">
            <!-- Logo -->
            <a class="navbar-brand" href="#"><img src="../../public/imgs/logo.png" alt="Logo"></a>
            <!-- /Logo -->
            
            <!-- Toggler Hamburger -->
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbars"
                aria-controls="navbars" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <!-- /Toggler Hamburger -->

            <!-- Menu -->
            <div class="collapse navbar-collapse" id="navbars">
                <ul class="navbar-nav me-auto mb-2 mb-md-0">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Link</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link disabled" aria-disabled="true">Disabled</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown"
                            aria-expanded="false">Dropdown</a>
                        <ul class="dropdown-menu">
                            <li><a class="dropdown-item" href="#">Action</a></li>
                            <li><a class="dropdown-item" href="#">Another action</a></li>
                            <li><a class="dropdown-item" href="#">Something else here</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
            <!-- /Menu -->

        </div>
    </nav>
</template>

<style scoped lang="scss">
    @import '../style/general.scss';
</style>
