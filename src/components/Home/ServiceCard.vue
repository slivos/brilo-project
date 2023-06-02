<template>
  <div
    class="d-flex flex-column justify-content-between align-items-center service-card gap-4 pb-4"
  >
    <div class="d-flex flex-column justify-content-center align-items-center text-center">
      <img :src="service.image_url" alt="service_img" class="img-fluid" />
      <span class="fw-bold my-3">{{ service.name }}</span>
      <p class="px-1">{{ truncate }}</p>
    </div>
    <ButtonPrimary text="ZJISTIT VÍCE" />
  </div>
</template>

<script setup>
import ButtonPrimary from '@/components/Button/Primary.vue'
import { computed } from 'vue'

const props = defineProps({
  service: Object
})

const truncate = computed(() => {
  if (props.service.description.length > 80) {
    return `${props.service.description.substring(0, 80)}...`
  } else {
    return props.service.description
  }
})
</script>

<style scoped>
.service-card {
  height: 585px;
  max-width: 316px;
}
</style>
