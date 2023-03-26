<script>
    export default {
        name: 'AppHero'
    }
</script>

<template>
    <section class="background">
        <div class="container">
            <h2>current series</h2>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use '../assets/styles/partials/variables.scss' as *;
    @use '../assets/styles/partials/mixins.scss' as *;
    .background {
        height: 25rem;
        background-image: url('../assets/img/jumbotron.jpg');
        background-size: cover
    }

    section .container{
        @include my-container(80rem);
        position: relative;
        height: 100%;

        h2 {
            background-color: $primary-color;
            position: absolute;
            bottom: 0;
            left: 0;
            transform: translate(0, 50%);
            padding: .75rem 1.875rem;
            font-size: 1.5rem;
            text-transform: uppercase;
            color: #fff;
        }
    }
</style>