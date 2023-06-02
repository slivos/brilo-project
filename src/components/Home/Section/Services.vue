<template>
  <div class="container-xxl px-4 px-xl-3 py-3 py-xl-0">
    <div class="d-flex flex-column justify-content-center align-items-center services-wrapper">
      <h2 class="fw-bold mb-4 text-center">Vyberte jednu z nabízených služeb</h2>
      <p class="description">
        Hlasu zkrátka nevratné duší indičtí půlkilometrová začali nutné už od středisko. Společných
        snažila líně budoucnost začne vloženy stal objevováním, umělé cílem starým dne větvičky
        názvy moři zabíjí.
      </p>
      <HomeTabs :tabs="tabs" class="mt-3 mt-xl-5 mb-5" />
      <div class="d-flex flex-row flex-wrap justify-content-center align-items-start gap-4">
        <ServiceCard v-for="service in filterServices" :key="service.id" :service="service" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
import HomeTabs from '@/components/Home/Tabs.vue'
import ServiceCard from '../ServiceCard.vue'
import services from '@/data/services.json'
import { useRoute } from 'vue-router'

const route = useRoute()

const tabs = [
  { name: 'VŠECHNO', hash: '#all' },
  { name: 'PAPÍROVÉ TAŠKY', hash: '#paper-bags' },
  { name: 'LÁTKOVÉ TAŠKY', hash: '#textil-bags' },
  { name: 'IGELITOVÉ TAŠKY', hash: '#plastic-bags' }
]

const filterServices = computed(() => {
  if (route.hash === '#paper-bags') {
    return services.filter((service) => {
      return service.name.toLowerCase().includes('papírové')
    })
  } else if (route.hash === '#textil-bags') {
    return services.filter((service) => {
      return service.name.toLowerCase().includes('látkové')
    })
  } else if (route.hash === '#plastic-bags') {
    return services.filter((service) => {
      return service.name.toLowerCase().includes('igelitové')
    })
  } else {
    return services
  }
})
</script>

<style scoped>
.services-wrapper {
  margin-bottom: 7rem;
}
.description {
  width: 70%;
  text-align: center;
  font-weight: 500;
}
</style>
