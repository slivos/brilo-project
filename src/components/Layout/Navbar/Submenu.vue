<template>
  <div class="submenu">
    <ul class="list-unstyled">
      <li class="submenu__item">
        <RouterLink to="#" class="link-primary-900 fw-bold">SUBMENU </RouterLink>
        <img src="@/assets/icons/rightarrow.svg" alt="right-arrow" class="submenu__arrow" />
      </li>
      <li class="submenu__item">
        <RouterLink to="#" class="link-primary-900 fw-bold">SUBMENU </RouterLink>
        <img src="@/assets/icons/rightarrow.svg" alt="right-arrow" class="submenu__arrow" />
      </li>
      <li class="submenu__item">
        <RouterLink to="#" class="link-primary-900 fw-bold">SUBMENU </RouterLink>
        <img src="@/assets/icons/rightarrow.svg" alt="right-arrow" class="submenu__arrow" />
      </li>
      <li class="submenu__item no--border">
        <RouterLink to="#" class="link-primary-900 fw-bold">SUBMENU </RouterLink>
        <img src="@/assets/icons/rightarrow.svg" alt="right-arrow" class="submenu__arrow" />
      </li>
    </ul>
  </div>
</template>

<style scoped>
.submenu {
  background: #ffffff;
  box-shadow: 0px 3px 15px rgba(0, 6, 91, 0.1);
  border-radius: 0.5rem;
  width: 15rem;
}
.submenu__item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  border-bottom: 1px solid #e7f0ff;
}

.submenu__arrow {
  display: none;
}
.submenu__item:hover > .submenu__arrow {
  display: inline-flex !important;
}

.no--border {
  border-bottom: none !important;
}
</style>
