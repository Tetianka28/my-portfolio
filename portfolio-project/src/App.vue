<script setup>
import { RouterLink, RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue';
import HeroMain from './components/HeroMain.vue'; 
import Footer from './components/Footer.vue';

</script>

<template> 
  <div class="wrapper grid grid-cols-12 gap-x-4 gap-y-0">

    <header class="col-span-12 sticky top-0 z-50">
      <NavBar />
    </header>

    <main class="col-span-12">
      <RouterView />
    </main>

    <!-- <footer class="col-span-12">
      <Footer />  
    </footer>  -->

  </div>
</template>

<style scoped>

</style>
