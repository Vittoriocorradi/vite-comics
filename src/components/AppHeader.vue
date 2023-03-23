<script>
    import AppHeaderLogo from './AppHeaderLogo.vue';
    import AppHeaderNav from './AppHeaderNav.vue';

    export default {
        name: 'Header',
        components: {
            AppHeaderLogo,
            AppHeaderNav
        }
    }
</script>

<template>
    <header>
        <div class="container-big">
            <AppHeaderLogo></AppHeaderLogo>
            <AppHeaderNav></AppHeaderNav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use "../components/styles/general.scss" as *;
  .container-big {
    @include my-container(80rem);
    @include my-flex(flex, space-between, center)
  }
</style>