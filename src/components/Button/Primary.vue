<template>
  <button class="btn button btn--primary fw-bold text-nowrap">
    {{ text }}
  </button>
</template>

<script setup>
const props = defineProps({
  text: String
})
</script>

<style scoped>
.btn--primary {
  color: var(--primary-900);
  background-color: var(--conversion-400);
  border: 1px solid var(--conversion-400) !important;
  transition: all 0.275s ease-in-out;
}

.btn--primary:hover {
  background-color: var(--conversion-500);
  border: 1px solid var(--conversion-500) !important;
  box-shadow: 0 2px 0 0 var(--conversion-600) !important;
}
</style>
