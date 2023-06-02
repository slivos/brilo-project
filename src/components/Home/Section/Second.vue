<template>
  <div class="container-xxl px-4 px-xl-3 py-3 py-xl-0">
    <BaseCard class="content-2">
      <template #body>
        <div
          class="d-flex flex-column justify-content-center justify-content-xl-start align-items-center align-items-xl-start align-self-xl-start content-2__text__wrapper"
        >
          <div class="d-flex flex-column align-items-center d-xl-inline-block mb-3 mb-xl-5">
            <h2 class="fw-bold mb-3">Nechte své peníze růst!</h2>
            <p class="description">
              V k žert planetu rysů obdivují stravování starověkého zebřičky u tahů zimující. Akcí
              a důkaz pomoci narozen muzea signálem – jižní využitelný uchu těžko. Dravcům vousům
              houba horu žijí mého vývojovou z společnosti nemigrují vy plná internetová, je
              charisma vnitrozemí, oceán a přijíždějí příbuzných zjevné, zemskou dá spolu. Moc král
              prokletí obyvatel holka ochlazení žít mimořádnými virů stejný či palec.
            </p>
          </div>
          <div class="d-flex justify-content-center justify-content-xl-start align-items-center">
            <ButtonPrimary text="ZAREGISTROVAT SE" />
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
</script>

<style scoped>
.content-2 {
  height: auto;
  gap: 2.5rem !important;

  @media (min-width: 1200px) {
    height: 679px;
  }
}

.content-2__text__wrapper {
  margin-top: 0px;
  @media (min-width: 1200px) {
    margin-top: 111.5px;
  }
}

.description {
  font-weight: 500;
}
</style>
