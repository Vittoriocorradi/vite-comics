<script>
    export default {
        name: 'Main',
        data() {
            return {
                content: '--> Content goes here <--'
            }
        }
    }
</script>

<template>
    <main>
        <div class="container-big">
        {{ content }}
        </div>
    </main>
</template>

<style lang="scss" scoped>
    @use "../components/styles/general.scss" as *;

    main {
        background-color: #1c1c1c;
        height: 130px;
        .container-big {
            @include my-container(80rem);
            @include my-flex(flex, start, center);
            color: #fff;
            font-size: 2em;
            height: 100%;
        }
    }
</style>