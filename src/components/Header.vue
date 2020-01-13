<template>
  <header class="site-header">
    <nav class="main-nav">
      <div class="logo">
        <a href="/"><Logo /></a>
        <span class="dates">
          Oslo<br />
          14&mdash;15th May<br />
          2020
        </span>
      </div>
      <div class="site-nav" :class="{open: open}">
        <div class="menu-toggle" @click="open = !open">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke-width="2"><line x1="3" y1="12" x2="24" y2="12"></line><line x1="3" y1="6" x2="24" y2="6"></line><line x1="3" y1="18" x2="24" y2="18"></line></svg>
        </div>
        <ul>
          <li @click="open = false"><router-link to="/">Home</router-link></li>
          <li @click="open = false"><router-link to="/schedule">Schedule</router-link></li>
          <li @click="open = false"><router-link to="/speakers">Speakers</router-link></li>
          <li @click="open = false"><router-link to="/info">Info</router-link></li>
          <li @click="open = false"><router-link to="/about">About</router-link></li>
          <li class="moon" @click="changeTheme()"><Moon /></li>
        </ul>
      </div>
    </nav>
  </header>
</template>

<script>
import Logo from '@/components/Logo.vue'
import Moon from '@/components/graphics/Moon.vue'

export default {
  components: {
    Logo,
    Moon
  },
  data: function() {
    return {
      open: false
    }
  },
  methods: {
    changeTheme: function() {
      document.body.classList.toggle('light-theme');
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
    width: 16rem;
    max-width: 30%;
    position: fixed;
    top: 4rem;
    right: -.9rem;
    z-index: 666;
    padding-bottom: 1.2rem;

    .dates {
      display: block;
      font-family: $monospace;
      font-size: 1rem;
      text-transform: uppercase;
      color: $color-main;
      position: relative;
      right: 1.6rem;
      text-align: right;
      line-height: 1.1;
      margin-top: -.5rem;
    }
    @media (max-width: $media-s) {
      position: absolute;
    }
  }

  .site-nav {
    transition: all .3s ease-in-out;
    text-align: center;
    width: 100%;

    ul {
      margin: 0;
      padding: 0;
      position: fixed;
      z-index: 666;
      top: 0;
      left: 0;
      right: 0;
      list-style: none;
      margin: 0;
      padding: .6rem 1rem;
      background: $color-black;
    }

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
      &.moon {
        position: relative;
        cursor: pointer;
      }
    }

    .menu-toggle {
      margin: 0;
      padding: 0;
      position: fixed;
      z-index: 1000;
      top: 0;
      left: 0;
      right: 0;
      display: none;
      background: $color-black;
      padding: .6rem 1rem;

      svg {
        width: 1em;
        height: 1em;
        stroke: $color-yellow;
      }
    }

    @media (max-width: $media-s) {
      ul {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        align-content: center;
        height: 100vh;
        padding-bottom: 5rem;
        transform: translateY(-100%);
        transition: transform .3s ease-in-out;
      }
      li {
        margin: 1.4rem auto;
        width: 100%;
        display: block;

        a {
          font-size: 1.4rem;
          display: block;
          width: 100%;
        }

        &.moon {
          display: block;
          align-self: flex-end;
          margin-top: auto;
        }

        &:first-child {
          margin-top: auto;
        }
      }
      .menu-toggle {
        display: block;
        cursor: pointer;
      }

      &.open {
        ul {
          transform: translateY(0);
        }
        .menu-toggle {
          margin: 0 auto 5rem;
          width: 100%;
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
.light-theme {
  .main-nav {
    .dates {
      color: $color-black;
    }
    .site-nav ul, .site-nav .menu-toggle {
      background: linear-gradient(45deg, $color-purple, $color-orange);
    }
  }
}
</style>
