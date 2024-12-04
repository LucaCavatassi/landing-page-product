<script>
    export default {
        data() {
            return {
                featuresLeft: [
                    {
                        title: 'Lunga Durata della Batteria',
                        description: 'Goditi ore di assistenza continua nella risoluzione dei bug grazie alla lunga durata della “batteria” (ovvero, la tua pazienza) della paperella di gomma.'
                    },
                    {
                        title:'Compatibilità Universale',
                        description: 'Funziona con tutti i linguaggi di programmazione e sistemi operativi, la paperella di gomma è l’unico strumento di debugging che non necessita di aggiornamenti.'
                    },
                    {
                        title:'Design Elegante',
                        description: 'Mostra con orgoglio il design elegante e raffinato della tua paperella di gomma, disponibile in vari colori per abbinarsi al tuo stile di programmatore.'
                    },
                ],
                featuresRight:
                [
                    {
                        title: 'Resistenza agli Spruzzi',
                        description: 'Perfetta per resistere ai piccoli incidenti con caffè e bevande, la tua paperella di gomma non teme schizzi, mantenendoti sempre pronto per il debugging.'
                    },
                    {
                        title:'Portabilità',
                        description: 'Leggera e facile da trasportare, la paperella di gomma può essere il tuo compagno di lavoro ovunque tu vada. Portala con te per un supporto costante.'
                    },
                    {
                        title:'Promemoria Anti-Stress',
                        description: 'Quando lo stress del codice diventa troppo, spremi la tua paperella di gomma per un rapido sollievo anti-stress, senza bisogno di software complicati.'
                    },
                ], 
            }
        }
    }
</script>
<template>
    <div id="features">
        <div class="container mt-5">
            <div class="row row-cols-1 row-cols-md-3">
                <div class="col justify-content-center align-items-center g-2 black-text body-font text-center">
                    <div class="mb-5" v-for="feature in featuresLeft">
                        <h4 class="px-5 px-md-3 fw-semibold mb-0">{{feature.title}}</h4>
                        <span>{{ feature.description }}</span>
                    </div>
                </div>
                <div class="col">Column</div>
                <div class="col justify-content-center align-items-center g-2 black-text body-font text-center">
                    <div class="mb-5" v-for="feature in featuresRight">
                        <h4 class="px-5 px-md-3 fw-semibold mb-0">{{feature.title}}</h4>
                        <span>{{ feature.description }}</span>
                    </div>
                </div>
            </div>
            <div class="row">
            </div>
        </div>
    </div>
</template>
<style scoped lang="scss">
@import '../style/general.scss';

span {
    font-size: 0.8rem;
}

</style>