<template>
  <header class="site-header">
    <nav class="main-nav">
      <div class="logo">
        <a href="/"><Logo /></a>
      </div>
      <ul class="site-nav">
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/schedule">Schedule</router-link></li>
        <li><router-link to="/speakers">Speakers</router-link></li>
        <li><router-link to="/about">About</router-link></li>
      </ul>
    </nav>
  </header>
</template>

<script>
import Logo from '@/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';
.site-header {
  padding: 0;
  font-family: $monospace;
}
.main-nav {
  .logo {
    width: 12rem;
    max-width: 60%;
    position: fixed;
    top: 1rem;
    right: -.8rem;
    z-index: 666;
  }

  .site-nav {
    position: fixed;
    z-index: 666;
    bottom: 0;
    list-style: none;
    margin: 0;
    padding: 0 0 1rem 0;
    transition: all .3s ease-in-out;
    text-align: center;
    width: 100%;

    li {
      display: inline-block;
      margin-right: 1.6rem;
    }
  }

  a {
    color: $color-link;
    text-decoration: none;
    position: relative;

    &:hover, &:focus {
      color: $color-link;
      font-weight: bold;
      border: none;
      padding: 0;
      margin: 0;
    }
    &:focus {
      color: $color-link;
    }
  }
}
</style>
