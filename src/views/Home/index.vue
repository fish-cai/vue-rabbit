<template>
  <div class="container">
    <HomeCategory/>
    <HomeBanner/>
  </div>
  <HomeNew/>
  <HomeHot/>
  <HomeProducts/>
</template>

<script setup>
import HomeBanner from './components/HomeBanner.vue'
import HomeCategory from './components/HomeCategory.vue'
import HomeHot from './components/HomeHot.vue'
import HomeNew from './components/HomeNew.vue'
import HomeProducts from './components/HomeProducts.vue'
</script>

<style>

</style>