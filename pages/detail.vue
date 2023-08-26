<template>
  <div class="constructor font-bold">
    <HeaderWeb />
    <p>hi ini adalah halaman detail</p>
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
