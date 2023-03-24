<script>
    import HeaderLogo from './HeaderLogo.vue';
    import HeaderNav from './HeaderNav.vue';

    export default {
        name: 'Header',
        components: {
            HeaderLogo,
            HeaderNav
        }
    }
</script>

<template>
    <header>
        <div class="container-big">
            <HeaderLogo></HeaderLogo>
            <HeaderNav></HeaderNav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use "../assets/styles/partials/mixins.scss" as *;
  .container-big {
    @include my-container(80rem);
    @include my-flex(flex, space-between, center)
  }
</style>