<template>
  <Navbar />
  <RouterView />
  <Footer />
</template>

<script setup>
import Navbar from '@/components/Layout/Navbar/index.vue'
import Footer from '@/components/Layout/Footer/index.vue'
</script>
