<script>
    import AppFooterNav from './AppFooterNav.vue';
    import AppFooterMenu from './AppFooterMenu.vue';
    import AppFooterSocial from './AppFooterSocial.vue';

    export default {
        name: 'Footer',
        components: {
            AppFooterNav,
            AppFooterMenu,
            AppFooterSocial
        }
    }
</script>

<template>
    <AppFooterNav></AppFooterNav>
    <AppFooterMenu></AppFooterMenu>
    <AppFooterSocial></AppFooterSocial>
</template>