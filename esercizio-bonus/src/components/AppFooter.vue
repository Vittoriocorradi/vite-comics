<script>
    import FooterNav from './FooterNav.vue';
    import FooterMenu from './FooterMenu.vue';
    import FooterSocial from './FooterSocial.vue';

    export default {
        name: 'Footer',
        components: {
            FooterNav,
            FooterMenu,
            FooterSocial
        }
    }
</script>

<template>
    <footer>
        <FooterNav></FooterNav>
        <FooterMenu></FooterMenu>
        <FooterSocial></FooterSocial>
    </footer>
</template>