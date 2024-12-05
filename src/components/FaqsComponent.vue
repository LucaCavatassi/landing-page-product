<script>
import FaqsAccordionComponent from './subComponents/faqsAccordionComponent.vue';
import infoGraphsComponent from './subComponents/infoGraphsComponent.vue';

    export default {
        components: {
            FaqsAccordionComponent,
            infoGraphsComponent
        },
        data() {
            return {
                questions: [
                    {
                        question: "Come posso utilizzare la paperella di gomma per il debugging?",
                        answer: "Il rubber duck debugging è semplice: spiega il tuo codice alla paperella di gomma come se fosse un collega. Descrivendo ogni passo, potresti individuare errori o capire meglio il problema. La paperella non risponde, ma ti aiuta a chiarire i tuoi pensieri."
                    },
                    {
                        question: "Quali sono i vantaggi di usare una paperella di gomma per i programmatori?",
                        answer: "La paperella di gomma aiuta i programmatori a pensare in modo critico e a verbalizzare i problemi. Questo processo può portare a nuove intuizioni e soluzioni. Inoltre, è un ottimo strumento antistress e aggiunge un tocco di personalità alla scrivania."
                    },
                    {
                        question: "Posso usare la paperella di gomma indipendentemente dal linguaggio di programmazione che utilizzo?",
                        answer: "Assolutamente sì! La paperella di gomma è universale e funziona con qualsiasi linguaggio di programmazione. Non importa se stai scrivendo in Python, Java, C++ o qualsiasi altro linguaggio, la paperella sarà sempre pronta ad ascoltarti."
                    },
                    {
                        question: "Quanto dettagliatamente devo spiegare il mio codice alla paperella di gomma?",
                        answer: "Dovresti spiegare ogni dettaglio del tuo codice. Più sei dettagliato, più è probabile che tu scopra errori o ottenga nuove prospettive. Questo processo ti costringe a rivedere attentamente ogni parte del tuo lavoro."
                    }
                ],
                infos: [
                    {
                        title: '100% Prodotto di Qualità',
                        description: 'Abbiamo anche la possibilità di ritiro direttamente dallo stagno',
                        logo: 'balloon'
                    },
                    {
                        title: 'Spedizione Gratuita',
                        description: 'Dal magazzino alla scrivania',
                        logo: 'bag-heart'
                    },
                    {
                        title: 'Rimborso Garantito',
                        description: 'Ti rimborsiamo se la paperella fa quack',
                        logo: 'handiplast'
                    },

                ]
            }
        }
    }
</script>

<template>
    <div id="faqs" class="container my-4">
        <!-- Head -->
        <h1 class="text-uppercase fw-bold text-left text-md-center mb-4">faqs</h1>
        <!-- /Head -->

        <!-- Accordion -->
        <div class="row">
            <!-- Img -->
            <div class="col-12 col-md-5 px-md-1 ">
                <img class="img-fluid" src="/imgs/single-image2.png" alt="girl-img">
            </div>
            <!-- /Img -->

            <!-- Accordion Component -->
            <div class="col-12 col-md-7 px-md-1">
                <FaqsAccordionComponent :questions="questions"/>
            </div>
            <!-- /Accordion Component -->
        </div>
        <!-- /Accordion -->

        <!-- Footer -->
        <div class="row my-5 pb-5">
            <div class="col-12 col-md-4" v-for="info in infos">
                <infoGraphsComponent :info="info"/>
            </div>
        </div>
        <!-- /Footer -->
    </div>
</template>

<style scoped lang="scss">
    @import '../style/general.scss';
    
    .col-md-5 {
        height: 100%;
        display: flex;
    }
    img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        display: block;
    }
</style>