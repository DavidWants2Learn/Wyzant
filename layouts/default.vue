<template>
  <div>

    <div class="Header">
      <TopHeader />
    </div>

    <nuxt />

    <div class="Footer">
      <BottomFooter />
    </div>

  </div>
</template>

<script>
import TopHeader from '~/components/global/Header.vue'
import BottomFooter from '~/components/global/Footer.vue'

export default {
  components:
    TopHeader,
    BottomFooter
}
</script>

<style>

</style>
