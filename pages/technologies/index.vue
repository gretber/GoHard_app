<template>
  <div class="about__us">
    <TechnologiesHeading />
    <TechnologiesContent />
  </div>
</template>
<script>
import TechnologiesHeading from '~/components/Technologies/TechnologiesHeading.vue'
import TechnologiesContent from '~/components/Technologies/TechnologiesContent.vue'
export default { components: { TechnologiesHeading, TechnologiesContent } }
</script>
<style scoped>
.about__us{
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
</style>
