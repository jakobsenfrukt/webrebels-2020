<template>
  <div class="home">
    <main>
      <p class="intro">A non-profit community conference for anyone who loves developing applications and services using web technology. Two days, one track, 16 speakers.</p>
      <section class="hero">
        <img src="https://www.cameronsworld.net/img/content/22/right-side/24.gif" /><br /><br />
        <h1 class="index-title">We'll be back in 2020</h1>
        <h2 class="index-subtitle subtitle">Join us in Oslo on 14th and 15th May</h2>
        <Tickets />
      </section>
      <!--div class="hero-image">
        <img src="https://2018.webrebels.org/static/webrebelBIG.759f990b.jpg" />
        <h1 class="hero-image-heading"><span class="heading-top">Class of Web Rebels 2020</span><span class="heading-bottom">we love you!</span></h1>
      </div-->
      <SpeakerList />
      <SponsorList />
    </main>
  </div>
</template>

<script>
import Tickets from '@/components/Tickets.vue'
import SpeakerList from '@/components/SpeakerList.vue'
import SponsorList from '@/components/SponsorList.vue'

export default {
  name: 'home',
  components: {
    Tickets,
    SpeakerList,
    SponsorList
  }
}
</script>

<style lang="scss" scoped>
@import '../css/variables.scss';
.intro {
  font-family: $monospace;
  margin: 0 0 6rem;
  width: $width-p;
  max-width: 70%;
  color: $color-white;
}
.index-title {
  font-size: 5rem;
}
.index-subtitle {
  font-size: 1,4rem;
  font-weight: 400;
}
.hero {
  min-height: 70vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.hero-image {
  width: 100%;
  margin: 0 auto 10rem;
  position: relative;

  &:after {
    content: " ";
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
}

  &-heading {
    margin: -5rem auto 0;
    font-size: 2rem;
    display: block;
    .heading-top {
      display: block;
      background: $color-black;
    }
    .heading-bottom {
      display: block;
      background: $color-black;
    }
  }
}
@media screen and (prefers-color-scheme: light) {
  .intro {
    color: $color-black;
  }
}
</style>
