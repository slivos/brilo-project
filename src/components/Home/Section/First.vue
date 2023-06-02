<template>
  <BaseCard class="content-1">
    <template #body>
      <div
        class="container-xxl px-4 px-xl-3 py-3 py-xl-0 d-flex flex-column-reverse flex-xl-row justify-content-between align-items-center content-1__container"
      >
        <img src="https://picsum.photos/648/456" alt="mock_image" class="img-fluid" />
        <div class="content-1__text__wrapper">
          <h2 class="fw-bold mb-3">Nechte své peníze růst!</h2>
          <p class="description mb-4 mb-xl-3 overflow-hidden">
            V k žert planetu rysů obdivují stravování starověkého zebřičky u tahů zimující. Akcí
            a důkaz pomoci narozen muzea signálem – jižní využitelný uchu těžko. Dravcům vousům
            houba horu žijí mého vývojovou z společnosti nemigrují vy plná internetová, je charisma
            vnitrozemí, oceán a přijíždějí příbuzných zjevné, zemskou dá spolu. Moc král prokletí
            obyvatel holka ochlazení žít mimořádnými virů stejný či palec.
          </p>
          <ul class="content-1__list overflow-hidden">
            <li class="description">
              Musel za až angličtinu látky nohy deprimovaná polokouli i roku map.
            </li>
            <li class="description">
              Těžko popsal, ještě zúročovat však, by čase musel mi nuly, ta naší.
            </li>
            <li class="description">
              Musel za až angličtinu látky nohy deprimovaná polokouli i roku map.
            </li>
            <li class="description">
              Těžko popsal, ještě zúročovat však, by čase musel mi nuly, ta naší.
            </li>
          </ul>
          <ButtonPrimary text="ZJISTIT VÍCE" class="mt-3 mt-xl-5" />
        </div>
      </div>
    </template>
  </BaseCard>
</template>

<script setup>
import BaseCard from '@/components/Base/Card.vue'
import ButtonPrimary from '@/components/Button/Primary.vue'
</script>

<style scoped>
.content-1 {
  height: auto;
  background-color: var(--primary-100) !important;

  @media (min-width: 1200px) {
    height: 679px;
  }
}

.content-1__container {
  max-height: none;
  gap: 2.5rem !important;

  @media (min-width: 1200px) {
    max-height: 456px;
    overflow: hidden;
  }
}

.content-1__text__wrapper {
  max-height: none;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  @media (min-width: 1200px) {
    max-height: 456px;
    display: inline-block;
  }
}

.description {
  max-height: 146px;
  font-weight: 500;
}

.content-1__list {
  max-height: 6rem;
  padding-left: 18px;
}
</style>
