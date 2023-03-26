<script>
    import MainHero from './MainHero.vue';
    import MainComicsList from './MainComicsList.vue';

    export default {
        name: 'Main',
        components: {
            MainHero,
            MainComicsList
        }
    }
</script>

<template>
    <main>
        <MainHero></MainHero>
        <MainComicsList></MainComicsList>
    </main>
</template>

<style lang="scss" scoped>

</style>