<template>
  <div id="app">
    <Oslo />
    <Header />
    <transition name="fade"><router-view/></transition>
    <Footer />
    <Smu />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import Oslo from '@/components/graphics/Oslo.vue'
import Smu from '@/components/graphics/Smu.vue'

export default {
  components: {
    Header,
    Footer,
    Oslo,
    Smu
  }
}
</script>

<style lang="scss">
@import 'css/main.scss';
</style>
