<template>
  <header class="site-header">
    <nav class="main-nav">
      <div class="logo">
        <a href="/"><Logo /></a>
        <span class="dates">Oslo 14&mdash;15th May 2020</span>
      </div>
      <ul class="site-nav" :class="{open: open}">
        <li class="menu-toggle" @click="open = !open">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2"><line x1="3" y1="12" x2="24" y2="12"></line><line x1="3" y1="6" x2="24" y2="6"></line><line x1="3" y1="18" x2="24" y2="18"></line></svg>
        </li>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/schedule">Schedule</router-link></li>
        <li><router-link to="/speakers">Speakers</router-link></li>
        <li><router-link to="/info">Info</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><span class="moon">&#9790;</span></li>
      </ul>
    </nav>
  </header>
</template>

<script>
import Logo from '@/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data: function() {
    return {
      open: false
    }
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
    max-width: 30%;
    position: fixed;
    top: 3rem;
    right: -.8rem;
    z-index: 666;
    padding-bottom: 1.2rem;

    .dates {
      font-family: $monospace;
      font-size: $font-s;
      text-transform: uppercase;
      color: $color-main;
      position: relative;
      right: -.2rem;
      text-align: right;
    }
    
    @media screen and (prefers-color-scheme: light) {
      .dates {
        color: $color-black;
      }
    }
    @media (max-width: $media-s) {
      position: absolute;
    }
  }

  .site-nav {
    position: fixed;
    z-index: 666;
    top: 0;
    left: 0;
    right: 0;
    list-style: none;
    margin: 0;
    padding: .6rem 1rem;
    background: $color-black;
    transition: all .3s ease-in-out;
    text-align: center;
    width: 100%;

    li {
      display: inline-block;
      padding: 0 1rem;
      text-align: center;

      a {
        color: $color-yellow;
        font-size: 1rem;
        text-transform: uppercase;
        letter-spacing: 2px;
      }
      .moon {
        color: $color-yellow;
        position: relative;
        right: 0;
      }
    }

    .menu-toggle {
      display: none;

      svg {
        width: 1em;
        height: 1em;
      }
    }

    @media screen and (prefers-color-scheme: light) {
      background: linear-gradient(45deg, $color-purple, $color-orange);
    }

    @media (max-width: $media-s) {
      li {
        display: none;
      }
      .menu-toggle {
        display: block;
        cursor: pointer;
      }

      &.open {
        li {
          display: block;
          margin: 2rem auto;
        }
        .menu-toggle {
          margin: 0 auto 5rem;
        }
      }
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
