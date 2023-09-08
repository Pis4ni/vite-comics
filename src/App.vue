<script>
import AppHeader from './components/Appheader.vue'
import AppContent from './components/AppContent.vue'
import AppNav from './components/AppNav.vue'
  export default {
    data(){
      return {
        title:'AppVue Working'
      }
    },
    components: {AppHeader, AppContent, AppNav}
  }
</script>

<template>
<main>
  <header class="deb">
    <AppHeader></AppHeader>
  </header>
  <section class="deb">
    <AppContent></AppContent>
  </section>
  <section class="deb">
    <AppNav></AppNav>
  </section>
  <h1>{{ title }}</h1>
</main>
</template>

<style lang="scss">
  body{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  .deb{
    border: 1px dashed red;
  }
</style>