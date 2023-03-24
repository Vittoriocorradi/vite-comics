<script>
  import AppHeader from './components/AppHeader.vue';
  import AppMain from './components/AppMain.vue';
  import AppFooter from './components/AppFooter.vue';

  export default {
    name: 'DC Comics',
    components: {
      AppHeader,
      AppMain,
      AppFooter
    }
  }
</script>

<template>
  <div class="container">
    <AppHeader></AppHeader>
    <AppMain></AppMain>
    <AppFooter></AppFooter>
  </div>
  
</template>

<style lang="scss" scoped>

</style>
