<template>
  <div class="main">
    <MainHeading />
    <MainAboutUs />
    <MainOurServices />
    <MainTechnologies />
    <MainPortfolio />
  </div>
</template>
<script>
import MainHeading from '~/components/Main/MainHeading.vue'
import MainAboutUs from '~/components/Main/MainAboutUs.vue'
import MainOurServices from '~/components/Main/MainOurServices.vue'
import MainTechnologies from '~/components/Main/MainTechnologies.vue'
import MainPortfolio from '~/components/Main/MainPortfolio.vue'
export default { components: { MainHeading, MainAboutUs, MainOurServices, MainTechnologies, MainPortfolio } }
</script>
<style>
.main {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
</style>
