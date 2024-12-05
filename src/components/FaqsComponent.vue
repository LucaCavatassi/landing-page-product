<script>
import FaqsAccordionComponent from './subComponents/faqsAccordionComponent.vue';

    export default {
        components: {
            FaqsAccordionComponent,
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
                ]
            }
        }
    }
</script>

<template>
    <div id="faqs" class="container p-5">
        <h1 class="text-uppercase fw-bold text-center">faqs</h1>
        <div class="row">
            <div class="col-12 col-md-4">
                <img class="img-fluid" src="/public/imgs/single-image2.png" alt="girl-img">
            </div>
            <div class="col-12 col-md-8">
                <FaqsAccordionComponent :questions="questions"/>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @import '../style/general.scss';

</style>