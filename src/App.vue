<template>
  <div>
   <Navbar/>
   <router-view/>
   <Data/>
   <Footer/>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'
import Data from '@/components/Data.vue'
  export default {
    components: {
      Footer,
      Navbar,
      Data
    }
  }
</script>

<style scoped>
  h1{
    font-size: xx-large;
    font-weight: bold;
    color: black;
  }

  body{
    background-color: #FFFFD0;
  }
</style>