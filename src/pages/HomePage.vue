<template>
  <HomeSectionHero />
  <HomeSectionFirst />
  <HomeSectionSecond />
  <HomeSectionServices />
</template>

<script setup>
import HomeSectionHero from '@/components/Home/Section/Hero.vue'
import HomeSectionFirst from '@/components/Home/Section/First.vue'
import HomeSectionSecond from '@/components/Home/Section/Second.vue'
import HomeSectionServices from '@/components/Home/Section/Services.vue'
import { onMounted } from 'vue'
import { useRoute, useRouter } from 'vue-router'

const route = useRoute()
const router = useRouter()

onMounted(() => {
  if (route.hash === '') {
    router.push({ hash: '#all' })
  }
})
</script>
