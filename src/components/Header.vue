<template>
    <div class="row">
        <div class="col-sm-12">
            <!-- <h3 class="text-center">Quotes Added</h3> -->
            <div class="progress">
                <div class="progress">
                    <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
                        :style="{width: (quoteCount / maxQuotes) * 100 + '%'}">
                        {{ quoteCount }} / {{ maxQuotes}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default {
        props: ['quoteCount', 'maxQuotes']
    }
</script>
<style scoped>
    h3 {
        color: white;
        text-shadow: 1px 1px grey;
    }
    .row {
        margin: 1.5em 0 0 0;
    }
    .progress-bar {
        background-color:#6DB193;
    }
</style>
