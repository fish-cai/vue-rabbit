<script setup>
import LayoutNav from './components/LayoutNav.vue'
import LayoutHeader from './components/LayHeader.vue'
import LayoutFooter from './components/LayFooter.vue'
</script>

<template>
  <LayoutNav />
  <LayoutHeader />
  <RouterView />
  <LayoutFooter />
</template>