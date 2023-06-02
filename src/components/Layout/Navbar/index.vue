<template>
  <div class="container-xxl px-4 px-xl-3">
    <div class="d-flex flex-row justify-content-between align-items-center py-4">
      <img src="@/assets/icons/logo.svg" alt="logo" />
      <img
        src="@/assets/icons/ham.svg"
        alt="hamburger-menu"
        class="d-flex d-xl-none navbar__menu__icon cursor-pointer"
        :class="{ 'icon--rotate--right': showMenu }"
        @click="displayMenu"
      />
      <nav class="d-none d-xl-flex flex-row justify-content-end align-items-center">
        <ul class="d-flex flex-row justify-content-end align-items-center gap-5 m-0 list-unstyled">
          <li class="navbar__menu__item">
            <RouterLink to="/about" class="link-primary-900 fw-bold">O NÁS</RouterLink>
          </li>
          <li
            class="d-flex align-items-center fw-bold cursor-pointer gap-1 position-relative navbar__submenu__opener"
          >
            SLUŽBY <img src="@/assets/icons/downarrow.svg" alt="down-arrow" />
            <LayoutNavbarSubmenu class="submenu" />
          </li>
          <li class="navbar__menu__item">
            <RouterLink to="/actualities" class="link-primary-900 fw-bold">AKTUALITY</RouterLink>
          </li>
          <li class="navbar__menu__item">
            <RouterLink to="/news" class="link-primary-900 fw-bold">NOVINKY</RouterLink>
          </li>
          <li class="navbar__menu__item">
            <RouterLink to="/contact" class="link-primary-900 fw-bold">KONTAKTY</RouterLink>
          </li>
        </ul>
      </nav>
    </div>
    <Transition>
      <LayoutNavbarMenu v-if="showMenu" @closing-menu="showMenu = false" />
    </Transition>
  </div>
</template>

<script setup>
import LayoutNavbarSubmenu from '@/components/Layout/Navbar/Submenu.vue'
import LayoutNavbarMenu from '@/components/Layout/Navbar/Menu.vue'
import { ref } from 'vue'

const showMenu = ref(false)

const displayMenu = () => {
  showMenu.value = !showMenu.value

  if (showMenu.value) {
    document.body.classList.add('menu-active')
  }
}
</script>

<style scoped>
.cursor-pointer {
  cursor: pointer;
}

.navbar__menu__icon {
  height: 25px;
  width: 25px;
  rotate: 0deg;
  transition: rotate 0.275s ease-in;
}

.icon--rotate--right {
  rotate: 90deg;
  transition: rotate 0.275s ease-in;
}

.navbar__menu__item {
  transition: box-shadow 0.275s ease-in-out;
}

.navbar__menu__item:hover {
  box-shadow: 0 5px 0 0 var(--conversion-400);
}

.navbar__menu__item__active {
  box-shadow: 0 5px 0 0 var(--conversion-400);
}

.submenu {
  position: absolute;
  top: 1.5rem;
  left: 0;
  z-index: 100;
  max-height: 0;
  overflow: hidden;
  opacity: 0;

  -webkit-transition: all 0.175s ease-in;
  transition: all 0.175s ease-in;
}

.navbar__submenu__opener:hover > .submenu {
  display: inline-block !important;
  max-height: 240px;
  opacity: 1;
}
.menu-active {
  position: relative;
}

.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
