<template>
  <div class="about__us">
    <PortfolioHeading />
    <PortfolioContent />
  </div>
</template>
<script>
import PortfolioHeading from '~/components/portfolio/PortfolioHeading.vue'
import PortfolioContent from '~/components/portfolio/PortfolioContent.vue'
export default { components: { PortfolioHeading, PortfolioContent } }
</script>
<style scoped>
.about__us{
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
</style>
