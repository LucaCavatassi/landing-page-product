<script>
import cardComponent from './subComponents/cardComponent.vue';
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination } from 'vue3-carousel';

export default {
    components: {
        cardComponent,
        Carousel,
        Slide,
        Pagination
    },
    data() {
        return {
            reviews: [
                {
                    description: "La paperella di gomma è diventata il mio strumento di debugging preferito. Spiegare i problemi al mio 'assistente' silenzioso mi ha aiutato a risolvere bug che altrimenti mi avrebbero fatto impazzire. È anche un ottimo antistress nelle giornate difficili!",
                    date: 'Feb 22, 2023',
                    name: 'David William'
                },
                {
                    description: "Non avrei mai immaginato quanto una semplice paperella di gomma potesse fare la differenza. È incredibile come verbalizzare i problemi davanti alla paperella mi aiuti a vedere soluzioni che prima non notavo. Inoltre, è carinissima sulla mia scrivania!",
                    date: "April 5, 2023",
                    name: "Emma Turner"
                },
                {
                    description: "Da quando ho adottato la paperella di gomma, il mio processo di debugging è migliorato notevolmente. La trovo molto utile per schiarirmi le idee e trovare errori nascosti. La porto sempre con me, ovunque vada!",
                    date: "April 18, 2023",
                    name: "Rachel Bryan"
                },
                {
                    description: "La mia paperella di gomma è il miglior collega che potessi chiedere. Sempre pronta ad ascoltare, mai giudicante. È sorprendente come qualcosa di così semplice possa essere così efficace nel risolvere problemi complessi. E non dimentichiamo che è anche adorabile!",
                    date: "May 22, 2023",
                    name: "Park C"
                },
            ]
        }
    }
}
</script>

<template>
    <div id="reviews">
        <div class="container mb-2 p-4">
            <h2 class="fw-bold text-center">Cosa ne pensano i nostri sviluppatori</h2>
            <!-- Main Wrapper -->
            <Carousel 
                :items-to-show="1" 
                :items-to-scroll="1" 
                :autoplay="4000" 
                wrap-around 
                pause-autoplay-on-hover
                :snapAlign="center - even" 
                :height="auto" 
                :breakpoints="{
                    768: { itemsToShow: 2 }, // On tablets, show 2 items per slide
                    1024: { itemsToShow: 3 } // On desktops, show 3 items per slide
                }">

                <!-- Slides -->
                <template #slides>
                    <Slide v-for="review in reviews" :key="review">
                        <div class="carousel__item">
                            <cardComponent :review="review" />
                        </div>
                    </Slide>
                </template>
                <!-- /Slides -->

                <!-- Pagination Dots -->
                <template #addons>
                    <Pagination />
                </template>
                <!-- /Pagination Dots -->
            </Carousel>
            <!-- /Main Wrapper -->
        </div>
    </div>
</template>

<style scoped lang="scss">
@import '../style/general.scss';
h2 {
    font-size: 3rem;
}

@media (min-width: 576px) {
    h2 {
        font-size: 2.5rem !important;
    }
}
</style>