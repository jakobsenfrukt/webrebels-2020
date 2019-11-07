<template>
  <div class="home">
    <main>
      <p class="intro">A non-profit community conference for anyone who loves developing applications and services using web technology. Two days, one track, 16 speakers.</p>
      <section class="hero">
        <h1 class="index-title">We'll be back in 2020</h1>
        <h2 class="index-subtitle subtitle">Join us in Oslo on 14th and 15th May</h2>
        <Tickets />
      </section>
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
@media screen and (prefers-color-scheme: light) {
  .intro {
    color: $color-black;
  }
}
</style>
