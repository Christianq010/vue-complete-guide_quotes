<template>
    <div class="container">
        <app-new-quote v-on:quoteAdded="newQuote"></app-new-quote>
        <app-quote-grid v-bind:quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue';
    import NewQuote from './components/NewQuote.vue';

    export default {
        data: function() {
            return {
                quotes: [
                    'This is just a random sample'
                ],
                maxQuotes: 10
            }
        },
        methods: {
            newQuote(quote) {
                this.quotes.push(quote);
            }
        },
        components: {
            appQuoteGrid: QuoteGrid,
            appNewQuote: NewQuote
        }
    }
</script>

<style>
    body {
        background-color: #FBE1B6;
        margin: 0;
    }
</style>
