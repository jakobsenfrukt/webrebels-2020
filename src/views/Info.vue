<template>
  <main class="simple-page info">
    <div class="hero">
      <h1 class="page-title">Practical info</h1>
      <p class="lead">The Web Rebels conference is a JavaScript conference and we are proud members of the <a href="https://jsconf.com/">JSConf family of events</a>. We are a conference for developers who love building applications and services using web technology.</p>
    </div>
    <Tickets />
    <h2>For the community, not for profit</h2>
    <p>We are a <a href="https://w2.brreg.no/enhet/sok/detalj.jsp?orgnr=997686659">registered not-for-profit organization</a> that is run by unpaid volunteers. If we make any profit from the conference we give 30% back to community groups throughout the Nordic region. Any questions you might have: <a href="mailto:boyhowdy@webrebels.org" target="_blank">shoot us an email</a> or find us on <a href="https://twitter.com/web_rebels/">Twitter</a>.</p>
    <div class="map">
      <div class="iframe-wrapper">
        <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d7998.600422083075!2d10.7527326!3d59.9213541!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x9ad90ca9da2b7f40!2sDansens%20Hus!5e0!3m2!1sen!2sno!4v1578950368739!5m2!1sen!2sno" width="600" height="450" frameborder="0" style="border:0;" allowfullscreen=""></iframe>
      </div>
    </div>
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

.map {
  max-width: $width-lead;
  margin: 2rem auto;
}
</style>