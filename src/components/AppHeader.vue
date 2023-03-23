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
    <AppHeaderLogo></AppHeaderLogo>
    <AppHeaderNav></AppHeaderNav>
</template>