<template>
  <div class="menu">
    <ul class="list-unstyled d-flex flex-column gap-4">
      <li class="menu__item">
        <RouterLink to="#" class="link-primary-900 fw-bold">MENU </RouterLink>
      </li>
      <li class="menu__item">
        <RouterLink to="#" class="link-primary-900 fw-bold">MENU </RouterLink>
      </li>
      <li class="menu__item">
        <RouterLink to="#" class="link-primary-900 fw-bold">MENU </RouterLink>
      </li>
      <li class="menu__item">
        <RouterLink to="#" class="link-primary-900 fw-bold">MENU </RouterLink>
      </li>
    </ul>
    <img src="@/assets/icons/xmark.svg" alt="x-mark" class="menu__close" @click="closeMenu" />
  </div>
</template>

<script setup>
import { onBeforeUnmount } from 'vue'

const emit = defineEmits(['closing-menu'])

const closeMenu = () => {
  emit('closing-menu')
  document.body.classList.remove('menu-active')
}
</script>

<style scoped>
.menu {
  width: 100%;
  min-height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  background: rgba(6, 235, 131, 0.9);
}

.menu__item {
  font-size: 2rem;
}

.menu__item:hover {
  text-decoration: line-through;
  text-decoration-thickness: 5px;
}

.menu__close {
  position: absolute;
  top: 2rem;
  right: 1.5rem;
  width: 25px;
  height: 25px;
  cursor: pointer;
}
</style>
