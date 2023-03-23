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
    <footer>
        <AppFooterNav></AppFooterNav>
        <AppFooterMenu></AppFooterMenu>
        <AppFooterSocial></AppFooterSocial>
    </footer>
</template>