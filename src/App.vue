<template>
  <v-app>
    <Navigationtop />
    <Searchfront />
    
    <v-content>
      <router-view></router-view>
    </v-content>

    <Footer />
  </v-app>
</template>
<script>

  // import HelloWorld from './components/HelloWorld';
  import Navigationtop from './components/shared/Navigation-top';
  import Searchfront from './components/shared/Search-front';
  import Footer from './components/shared/Footer';

  export default {
    name: 'App',
    components: {
        Navigationtop,
        Searchfront,
        Footer
    },
    data() {
      return {
   
      }
    }
  }
</script>
<style scoped>
  
</style>
