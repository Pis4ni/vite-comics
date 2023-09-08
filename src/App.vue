<script>
import AppHeader from './components/Appheader.vue'
import AppContent from './components/AppContent.vue'
import AppNav from './components/AppNav.vue'
import AppMap from './components/AppMap.vue'
import AppFooter from './components/AppFooter.vue'
  export default {
    data(){
      return {
        title:'AppVue Working'
      }
    },
    components: {AppHeader, AppContent, AppNav, AppMap, AppFooter }
  }
</script>

<template>
<main>
  <header>
    <AppHeader></AppHeader>
  </header>
  <section>
    <AppContent></AppContent>
  </section>
  <section>
    <AppNav></AppNav>
  </section>
  <section>
    <AppMap></AppMap>
  </section>
  <footer>
    <AppFooter></AppFooter>
  </footer>
</main>
</template>

<style lang="scss">
  body{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  main{
    height: 100vh;
  }
</style>