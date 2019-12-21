<template>
  <div id="app">
    <Oslo />
    <Header />
    <transition name="fade">
      <router-view />
    </transition>
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import Oslo from '@/components/graphics/Oslo.vue'

export default {
  components: {
    Header,
    Footer,
    Oslo
  },
  beforeMount: function() {
    if (window.matchMedia('(prefers-color-scheme: light)').matches) {
      document.body.classList.add('light-theme');
    }
  }
}
</script>

<style lang="scss">
@import 'css/main.scss';
</style>
