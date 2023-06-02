<template>
  <button class="btn button btn--secondary fw-bold text-nowrap">
    {{ text }}
  </button>
</template>

<script setup>
const props = defineProps({
  text: String
})
</script>

<style scoped>
.btn--secondary {
  color: var(--conversion-400);
  background-color: white;
  border: 1px solid var(--primary-100) !important;
  box-shadow: 0px 3px 15px rgba(0, 6, 91, 0.1);
  border-radius: 0.5rem;
  transition: all 0.275s ease-in-out;
}

.btn--secondary:hover {
  color: var(--primary-900);
  background-color: var(--primary-100);
  box-shadow: 0px 5px 15px rgba(0, 6, 91, 0.3);
  border-radius: 0.5rem;
}

.active {
  color: white;
  background-color: var(--primary-500);
}
</style>
