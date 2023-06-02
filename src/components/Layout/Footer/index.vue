<template>
  <div class="container-xxl px-4 px-xl-3">
    <div
      class="d-flex flex-column flex-xl-row justify-content-between align-items-center py-3 py-xl-5 footer-wrapper"
    >
      <img src="@/assets/icons/logo-bigger.svg" />
      <ul class="d-flex flex-row justify-content-center align-items-center list list-unstyled m-0">
        <li class="footer__menu__item">
          <RouterLink to="#" class="link-conversion-400 fw-bold">První proklik</RouterLink>
        </li>
        <li class="footer__menu__item">
          <RouterLink to="#" class="link-conversion-400 fw-bold">Druhý proklik</RouterLink>
        </li>
        <li class="footer__menu__item">
          <RouterLink to="#" class="link-conversion-400 fw-bold"> Třetí proklik</RouterLink>
        </li>
      </ul>
      <div class="copyright">© 2022 Thalion All rights reserved.</div>
    </div>
  </div>
</template>

<style scoped>
.footer-wrapper {
  border-top: 0.5rem solid var(--primary-100);
  gap: 2rem;
}
.list {
  gap: 2rem;

  @media (min-width: 1200px) {
    gap: 2.5rem;
  }
}
.copyright {
  font-weight: 500;
}

.footer__menu__item {
  transition: box-shadow 0.275s ease-in-out;
}

.footer__menu__item:hover {
  box-shadow: 0 5px 0 0 var(--primary-500);
}
</style>
