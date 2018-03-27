<template>
    <div class="row">
        <form>
            <div class="form-group">
                <label>Quote</label>
                <textarea class="form-control" v-model="quote"></textarea>
                <button class="btn-primary" v-on:click.prevent="createNew">Add Quote</button>
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
    }
    textarea {
        margin: 1em auto;
        width: 60%;
    }
    button {
        margin: 1em;
    }

</style>


