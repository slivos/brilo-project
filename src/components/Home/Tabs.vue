<template>
  <div class="gap-4 tabs">
    <button
      v-for="(tab, index) in tabs"
      :key="index"
      class="btn button btn--secondary fw-bold text-nowrap"
      :class="{ active: currentTab === index }"
      @click="setHash(tab)"
    >
      {{ tab.name }}
    </button>
  </div>
</template>

<script setup>
import { watchEffect, ref } from 'vue'
import { useRouter, useRoute } from 'vue-router'

const props = defineProps({
  tabs: Array
})

const router = useRouter()
const route = useRoute()

const currentTab = ref(0)

watchEffect(() => {
  const tabIndex = props.tabs.findIndex((tab) => tab.hash === route.hash)
  currentTab.value = tabIndex
})

const setHash = (tab) => {
  if (tab) {
    router.push({ hash: `${tab.hash}` })
  }
}
</script>

<style scoped>
.tabs {
  display: grid;
  grid-template-columns: 1fr 1fr;

  @media (min-width: 1200px) {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

.btn--secondary {
  color: var(--conversion-400);
  background-color: white;
  border: 1px solid var(--primary-100) !important;
  box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.1) !important;
}

.btn--secondary:hover {
  color: var(--primary-900);
  background-color: var(--primary-100);
  border: 1px solid var(--primary-100) !important;
  box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.25) !important;
}

.active {
  color: white;
  background-color: var(--primary-500);
  border: 1px solid var(--primary-500) !important;
}
</style>
