<template>
    <div class="col-md-4">
        <div class="panel panel-default">
            <div class="panel-body quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['quotes']
    }
</script>

<style>
    .panel-body{
        font-family: 'Lato', sans-serif;
        font-size: 24px;
        color: #6e6e6e;
    }
    .quote:hover {
        background-color: palevioletred;
    }
</style>
