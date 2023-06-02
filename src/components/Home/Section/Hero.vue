<template>
  <div class="container-xxl px-4 px-xl-3">
    <BaseCard class="hero">
      <template #body>
        <div
          class="d-flex flex-column justify-content-start align-items-center align-items-xl-start w-100"
        >
          <div class="mb-3 mb-xl-5">
            <h1 class="fw-bold mb-3">Hlavní nadpis webu</h1>
            <p class="hero__text mb-0">
              V k žert planetu rysů obdivují stravování starověkého zebřičky u tahů zimující. Akcí
            </p>
            <p class="hero__text">a důkaz pomoci narozen muzea signálem.</p>
          </div>
          <div class="d-flex justify-content-start align-items-center gap-3 gap-xl-4">
            <ButtonSecondary text="VÍCE INFORMACÍ" class="me-2" />
            <ButtonPrimary text="POPTAT NABÍDKU" />
          </div>
        </div>
        <img src="https://picsum.photos/648/456" alt="mock_image" class="img-fluid" />
      </template>
    </BaseCard>
  </div>
</template>

<script setup>
import BaseCard from '@/components/Base/Card.vue'
import ButtonPrimary from '@/components/Button/Primary.vue'
import ButtonSecondary from '@/components/Button/Secondary.vue'
</script>

<style scoped>
.hero {
  padding-bottom: 3rem;

  @media (min-width: 1200px) {
    padding-bottom: 6rem;
  }
}
.hero__text {
  font-weight: 500;
}
</style>
