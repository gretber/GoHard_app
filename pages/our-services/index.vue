<template>
  <div class="our_services">
    <OurServicesHeading />
    <OueServicesContent />
  </div>
</template>
<script>
import OurServicesHeading from '~/components/OurServices/OurServicesHeading.vue'
import OueServicesContent from '~/components/OurServices/OurServicesContent.vue'
export default { components: { OurServicesHeading, OueServicesContent } }
</script>
<style scoped>
.our_services{
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
}
</style>
