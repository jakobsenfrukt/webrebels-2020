<template>
  <main class="about">
    <h1 class="page-title">About</h1>
    <section>
      <h2>What happened to Web Rebels 2019?</h2>
      <p>Usually, after wrapping up the conference, we secure our venue for the following year straight away. This time however, we ran into an unexpected challenge: none of the dates available worked for us.</p>
      <p>We went looking for alternatives but ultimately, nothing fit what we were looking for. When you run a conference, you always work within certain constraints, and this time, we couldn’t make it work.</p>
      <p>As a consequence, there will be no Web Rebels in 2019. You may have guessed this already.</p>
      <p>The good news is that we have the dates and the venue we want for 2020.</p>
    </section>
    <Tickets />
  </main>
</template>

<script>
import Tickets from '@/components/Tickets.vue'

export default {
  components: {
    Tickets
  }
}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
</style>