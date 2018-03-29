<template>
    <div class="row">
        <app-quote v-for="(quote, index) in quotes" :key="index" v-on:click.native="deleteQuote(index)">
            {{quote}}
        </app-quote>
    </div>
</template>

<script>
    import Quote from './Quote.vue';
    export default {
        props: ['quotes'],
        components: {
            appQuote: Quote
        },
        methods: {
            deleteQuote(index) {
                this.$emit('quoteDeleted', index);
                console.log(index);
            }
        }
    }
</script>

<style scoped>
    .row {
        margin: 2em auto;
    }
</style>


