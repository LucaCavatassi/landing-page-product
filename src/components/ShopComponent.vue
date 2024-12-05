<script>
    import ShopCardComponent from './subComponents/shopCardComponent.vue';

    export default {
        components: {
            ShopCardComponent
        },
        data() {
            return {

            }
        }
    }

</script>

<template>
    <div id="shop" class="p-4">
        <div class="container">
            <!-- Infotext -->
            <div class="text-center info-text">
                <h1 class="fw-bold">La collezione di paperelle</h1>
                <p>Una paperella per ogni stile di programmazione</p>
            </div>
            <!-- /Infotext -->
            <div class="row">
                <div class="col-12 col-md-4">
                    <ShopCardComponent/>
                </div>
            </div>
        </div>
        
    </div>
</template>

<style scoped lang="scss">
    @import '../style/general.scss';

    #shop {
        background-color: $grey;
        .info-text {
            p {
                font-size: 0.8rem;
            }
        }
    }

    @media (min-width: 576px) {
        .info-text {
            p {
                font-size: 1rem!important;
            }
        }
    }

</style>