<template>
  <div class="constructor font-bold">
    <HeaderWeb />
    <p class="text-lg .box">hi ini adalah profil</p>
    <FooterWeb />
  </div>
</template>

<script>
import FooterWeb from '../components/FooterWeb.vue'
import HeaderWeb from '../components/HeaderWeb.vue'
export default {
  components: { FooterWeb, HeaderWeb }
}
</script>
