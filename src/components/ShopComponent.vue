<script>
    import ShopCardComponent from './subComponents/shopCardComponent.vue';

    export default {
        components: {
            ShopCardComponent
        },
        data() {
            return {
                items: [
                    {
                        price: "15",
                        name: "Cool-duck",
                        img_path: "/imgs/product-item1.png"
                    },
                    {
                        price: "29",
                        name: "Classic-duck",
                        img_path: "/imgs/product-item2.png"
                    },
                    {
                        price: "69",
                        name: "Bat-duck",
                        img_path: "/imgs/product-item3.png"
                    }
                ]
            }
        }
    }

</script>

<template>
    <div id="shop">
        <div class="container">
            <!-- Infotext -->
            <div class="text-center info-text p-4">
                <h1 class="fw-bold">La collezione di paperelle</h1>
                <p>Una paperella per ogni stile di programmazione</p>
            </div>
            <!-- /Infotext -->
            <!-- Cards -->
            <div class="row gx-1">
                <div v-for="item in items" class="col-12 col-md-4">
                    <ShopCardComponent :item="item"/>
                </div>
            </div>
            <!-- /Cards -->
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