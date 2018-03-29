<template>
    <div class="container">
        <app-header v-bind:quoteCount="quotes.length" v-bind:maxQuotes="maxQuotes"></app-header>
        <app-new-quote v-on:quoteAdded="newQuote"></app-new-quote>
        <app-quote-grid v-bind:quotes="quotes" v-on:quoteDeleted="deleteQuote"></app-quote-grid>
        <!-- Info Window -->
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-success alert-edit">
                    <p>Click on a Quote to Delete it!</p>
                </div>
            </div>
        </div>
        <!-- /end of Info Window -->
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue';
    import NewQuote from './components/NewQuote.vue';
    import Header from './components/Header.vue';

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
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1);
            }
        },
        components: {
            appQuoteGrid: QuoteGrid,
            appNewQuote: NewQuote,
            appHeader: Header
        }
    }
</script>

<style>
    body {
        background-color: #FBE1B6;
        margin: 0;
        font-family: 'Lato', sans-serif;
    }

    .alert-edit {
        background-color: #A7EFE9;
        color: white;
    }

</style>
