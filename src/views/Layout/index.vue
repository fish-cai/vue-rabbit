<script setup>
import LayoutNav from './components/LayoutNav.vue'
import LayoutHeader from './components/LayHeader.vue'
import LayoutFooter from './components/LayFooter.vue'
import LayoutFixed from './components/LayoutFixed.vue'
import {onMounted} from 'vue'

import { useCategoryStore } from '@/stores/category'

const categoryStore = useCategoryStore()

onMounted(() => {
  categoryStore.getCategory()
})
</script>

<template>
  <LayoutNav />
  <LayoutHeader />
  <RouterView />
  <LayoutFooter />
  <LayoutFixed/>
</template>