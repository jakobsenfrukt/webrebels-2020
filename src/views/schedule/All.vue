<template>
  <main class="schedule-page">
    <div class="hero">
      <h1 class="page-title">Schedule</h1>
      <p class="lead">Check out this awesome schedule.</p>
      <Tickets />
    </div>
    <div class="jump"><a href="#friday">Jump to Friday</a></div>
    <div class="schedule">
      <div class="schedule-day day1" id="thursday">
        <h2 class="section-heading schedule-title">Thursday May 14th</h2>
        <div class="contents-wrapper">
          <div class="contents">
            <div class="event info">
              <div class="when">08:00</div>
              <div class="what">
                <h4 class="event-title">Registration and breakfast</h4>As the tradition goes, no need for that hotel
                breakfast. Join us for a Rebel breakfast instead.
              </div>
            </div>
            <div class="event talk">
              <div class="when">09:00</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Patricia Aas</a></h4>Reading other peoples code
              </div>
            </div>
            <div class="event talk">
              <div class="when">09:45</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Mathieu &#x27;p01&#x27; Henri</a></h4>A testing story in 3 acts
              </div>
            </div>
            <div class="event pause">
              <div class="when">10:30</div>
              <div class="what">
                <h4 class="event-title">Coffee/tea break</h4>
              </div>
            </div>
            <div class="event talk">
              <div class="when">11:00</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Maxim Salnikov</a></h4>Service Worker: taking the best from the past experience for
                the bright future of PWAs
              </div>
            </div>
            <div class="event talk">
              <div class="when">11:45</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Tor Martin Storsletten, Tom Widerøe and Lotte Johansen</a></h4>How to make accessible
                web when the ideal does not match reality?
              </div>
            </div>
            <div class="event pause">
              <div class="when">12:30</div>
              <div class="what">
                <h4 class="event-title">Lunch</h4>
                Across the river at <a href="/about#nedre_foss_info">Nedre Foss Gård.</a>
              </div>
            </div>
            <div class="event talk">
              <div class="when">13:30</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Sigurd Schneider</a></h4>Inside V8: The choreography of Ignition and TurboFan
              </div>
            </div>
            <div class="event talk">
              <div class="when">14:15</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Ivan Jovanovic</a></h4>Thinking Reactive in JavaScript
              </div>
            </div>
            <div class="event pause">
              <div class="when">15:00</div>
              <div class="what">
                <h4 class="event-title">Coffee/tea break</h4>
              </div>
            </div>
            <div class="event talk">
              <div class="when">15:30</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Michael Geers</a></h4>Micro Frontends - Think Smaller, Avoid the Monolith, Love the
                Backend
              </div>
            </div>
            <div class="event talk">
              <div class="when">16:15</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Stefan Judis</a></h4>What the v...DOM?
              </div>
            </div>
            <div class="event talk">
              <div class="when">17:00</div>
              <div class="what">
                <h4 class="event-title"><a href="/speakers" class="speaker-name">Martin Splitt</a></h4>JS in parallel - heavy duty in the browser
              </div>
            </div>
            <div class="event party">
              <div class="when">18:00</div>
              <div class="what">
                <h4 class="event-title">Conference dinner and social gathering</h4>
                About 3 minutes walk down the road to <a href="/about#party_info">Ingensteds</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="schedule-day day2" id="friday">
        <h2 class="section-heading schedule-title">Friday May 15th</h2>
        <div class="contents-wrapper">
          <div class="contents">
            <div class="event info">
              <div class="when">08:00</div>
              <div class="what">
                <h4 class="event-title">Breakfast</h4>
              </div>
            </div>
            <div class="event talk">
              <div class="when">09:00</div>
              <div class="what">
                <h4 class="event-title">John Papa</h4>Readable Code
              </div>
            </div>
            <div class="event talk">
              <div class="when">09:45</div>
              <div class="what">
                <h4 class="event-title">Emil Bay</h4>
                Hand-crafting WebAssembly
              </div>
            </div>
            <div class="event pause">
              <div class="when">10:30</div>
              <div class="what">
                <h4 class="event-title">Coffee/tea break</h4>
              </div>
            </div>
            <div class="event talk">
              <div class="when">11:00</div>
              <div class="what">
                <h4 class="event-title">Ernie Turner</h4>
                Dodging Web Crypto API Landmines
              </div>
            </div>
            <div class="event talk">
              <div class="when">11:45</div>
              <div class="what">
                <h4 class="event-title">Luciano Mammino</h4>
                Cracking JWT tokens: a tale of magic, Node.JS and parallel
                computing
              </div>
            </div>
            <div class="event pause">
              <div class="when">12:30</div>
              <div class="what">
                <h4 class="event-title">Lunch</h4>
                Right next door at <a href="/about#mathallen_info">Mathallen.</a>
              </div>
            </div>
            <div class="event talk">
              <div class="when">13:30</div>
              <div class="what">
                <h4 class="event-title">Monika Kedrova</h4>Building virtual worlds with web technologies
              </div>
            </div>
            <div class="event talk">
              <div class="when">14:15</div>
              <div class="what">
                <h4 class="event-title">Madlaina Kalunder</h4>Building a ray tracer in Javascript
              </div>
            </div>
            <div class="event pause">
              <div class="when">15:00</div>
              <div class="what">
                <h4 class="event-title">Coffee/tea break</h4>
              </div>
            </div>
            <div class="event talk">
              <div class="when">15:30</div>
              <div class="what">
                <h4 class="event-title">Michaela Lehr</h4>Using New Web APIs For Your Own Pleasure – How I Wrote New
                Features For My Vibrator using the Web Bluetooth API and the Web Audio API
              </div>
            </div>
            <div class="event talk">
              <div class="when">16:15</div>
              <div class="what">
                <h4 class="event-title">Joe Karlsson</h4>Building High Performance React Applications
              </div>
            </div>
            <div class="event party">
              <div class="when">17:00</div>
              <div class="what">
                <h4 class="event-title">Group photo - end</h4>As tradition goes we take a group photo of everyone
              </div>
            </div>
          </div>
        </div>
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

<style lang="scss" scoped>
@import '@/css/variables.scss';

.schedule {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  max-width: $width-full;
  margin: 0 auto 5rem;

  &-day {
    width: 45%;

    @media (max-width: $media-s) {
      width: 100%;
    }
  }

  &-title {
    font-size: 2.2rem;
  }

  .event {
    display: flex;
    margin-bottom: 1rem;

    .when {
      font-size: 1.2rem;
      width: 6rem;
      padding-right: 1rem;
      font-family: $monospace;
    }
    .what {
      width: 100%;
      font-family: $monospace;

      h4 {
        font-family: $sans-serif;
      }
    }
    &-title {
      margin: 0;
      line-height: 1.3;
      text-align: left;
      font-size: 1.4rem;
    }
    &.info {
      border-top: 2px solid $color-pink;
      border-bottom: 2px solid $color-pink;
      padding: .5rem 0;
     .event-title {
        color: $color-pink;
      }
    }
    &.pause {
      border-top: 2px solid $color-yellow;
      border-bottom: 2px solid $color-yellow;
      padding: .5rem 0;
     .event-title {
        color: $color-yellow;
      }
    }
    &.party {
      border-top: 2px solid $color-pink;
      border-bottom: 2px solid $color-pink;
      padding: .5rem 0;
      .event-title {
        color: $color-pink;
      }
    }
  }
}
.jump {
  font-size: $font-s;
  margin-bottom: 2rem;
  text-align: right;

  display: none;
}
@media (max-width: $media-s) {
  .jump {
    display: block;
  }
  .schedule-day {
    margin-bottom: 4rem;
    h2 {
      font-size: 1.8rem;
    }
  }
}
@media screen and (prefers-color-scheme: light) {
  .schedule .event.pause {
    border-top: 2px solid $color-orange;
    border-bottom: 2px solid $color-orange;
    padding: .5rem 0;
    .event-title {
      color: $color-orange;
    }
  }
}
.light-theme {
  .schedule .event.pause {
    border-top: 2px solid $color-orange;
    border-bottom: 2px solid $color-orange;
    padding: .5rem 0;
    .event-title {
      color: $color-orange;
    }
  }
}
</style>
