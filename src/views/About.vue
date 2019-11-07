<template>
  <main class="simple-page about">
    <div class="hero">
      <h1 class="page-title">About</h1>
      <p class="lead">The Web Rebels conference is a JavaScript conference and we are proud members of the <a href="https://jsconf.com/">JSConf family of events</a>. We are a conference for developers who love building applications and services using web technology.</p>
    </div>
    <h2>For the community, not for profit</h2>
    <p>We are a <a href="https://w2.brreg.no/enhet/sok/detalj.jsp?orgnr=997686659">registered not-for-profit organization</a> that is run by unpaid volunteers. If we make any profit from the conference we give 30% back to community groups throughout the Nordic region. Any questions you might have: <a href="mailto:boyhowdy@webrebels.org" target="_blank">shoot us an email</a> or find us on <a href="https://twitter.com/web_rebels/">Twitter</a>.
    <p>We invite <a href="/speakers">16 speakers</a>. We do not have a CFP and our <a href="/policies">policy</a> is that speakers at the conference get paid for their travel and accommodation. We do not sell speaker slots and we do not accept sales pitches masked as presentations.</p>
    <h2>Code of Conduct</h2>
    <p>We want these couple of days to be truly enjoyable for everyone. Attendees, speakers, sponsors and volunteers must all respect the JSConf Code of Conduct. If anything happens that we should know about, contact a member of the crew.</p>
    <h2>Rebel Crew</h2>
    <p>The volunteers working to bring you the 5th Web Rebels Conference are:</p>
    <ul>
      <li>Alexandra Leisse (@troubalex)</li>
      <li>Anders Olsen Sandvik (@Andersos)</li>
      <li>Bodil Stokke (@bodil)</li>
      <li>Espen Dalløkken (@leftieFriele)</li>
      <li>Richard Walker (@digitalsadhu)</li>
      <li>Trygve Lie (@trygve-lie)</li>
    </ul>
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