<template>
  <div class="home">
    <main>
      <p class="intro">A non-profit community conference for anyone who loves developing applications and services using web technology. Two days, one track, 16 speakers.</p>
      <section>
        <h1 class="index-title">We'll be back in 2020</h1>
        <h2 class="subtitle">Join us in Oslo on 14th and 15th May</h2>
        <p class="lead">We’re putting the same effort and love into the conference and its line-up that you are used to from previous years.</p>
      </section>
      <Tickets />
      <SpeakerList />
    </main>
  </div>
</template>

<script>
import Tickets from '@/components/Tickets.vue'
import SpeakerList from '@/components/SpeakerList.vue'

export default {
  name: 'home',
  components: {
    Tickets,
    SpeakerList
  }
}
</script>

<style lang="scss" scoped>
@import '../css/variables.scss';
.intro {
  font-family: $monospace;
  line-height: 1.4;
  margin-bottom: 3rem;
  max-width: 30rem;
}
.index-title {
  font-size: 5rem;
}
</style>
