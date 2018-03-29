<template>
    <div class="row">
        <form>
            <div class="form-group">
                <textarea class="form-control" v-model="quote"></textarea>
                <button class="btn-primary text-uppercase" v-on:click.prevent="createNew">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        data: function () {
            return {
                quote: ''
            };
        },
        methods: {
            createNew() {
                this.$emit('quoteAdded', this.quote);
                this.quote = '';
            }
        }
    }
</script>

<style scoped>
    .row {
        margin: 2em auto;
        text-align: center;
        font-family: 'Lato', sans-serif;
    }
    textarea {
        margin: 1em auto;
        font-size: 25px;
        color: lightgrey;
        width: 60%;
        box-shadow: 0 16px 28px 0 rgba(0,0,0,.05), 0 25px 55px 0 rgba(0,0,0,.06);
    }
    button {
        font-size: 25px;
        font-weight: 900;
        margin: 1em;
        width: 250px;
        min-height: 50px;
        background: #583b8a;
        position: relative;
        box-shadow: 0 16px 28px 0 rgba(0,0,0,.05), 0 25px 55px 0 rgba(0,0,0,.06);
    }
    button:hover {
        background: #583b8a;
    }

</style>


