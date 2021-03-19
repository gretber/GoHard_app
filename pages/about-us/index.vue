<template>
  <div class="about__us">
    <AboutUsHeading />
    <AboutUsContent />
  </div>
</template>
<script>
import AboutUsHeading from '~/components/AboutUs/AboutUsHeading.vue'
import AboutUsContent from '~/components/AboutUs/AboutUsContent.vue'
export default { components: { AboutUsHeading, AboutUsContent } }
</script>
<style scoped>
 .about__us{
   display: flex;
   flex-direction: column;
   justify-content: flex-start;
   align-items: center;
 }
</style>
