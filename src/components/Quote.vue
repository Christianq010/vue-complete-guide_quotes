<template>
    <div class="col-md-4">
        <div class="">
            <div class="panel-body quote-text quote">
                <slot></slot>
            </div>
        </div>
    </div>
</template>

<script>
</script>

<style>
    .panel-body {
        font-family: 'Lato', sans-serif;
        color: #fff;
        width: 100%;
        overflow: hidden;
        max-width: 560px;
        min-height: 390px;
        margin: 50px;
        background: palevioletred;
        position: relative;
        box-shadow: 0 16px 28px 0 rgba(0,0,0,.22), 0 25px 55px 0 rgba(0,0,0,.21);
    }
    .quote-text {
        font-size: 48px;
        font-weight: 900;
        line-height: 55px;
    }
    .quote {
        padding: 15px;
        /* width: calc(560px - 140px); */
    }
    .quote:hover {
        background-color: #7FDFD4;
    }
    .author-text {
        bottom: 15px;
        font-size: 14px;
        font-weight: 500;
        position: absolute;
    }
</style>
