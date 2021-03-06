<template>
  <div class="home">
    <main>
      <p class="intro"><a href="/about">Web Rebels</a> is a non-profit community conference for anyone who loves developing applications and services using web technology. Two days, one track, 16 speakers.</p>
      <section class="hero">
        <h1 class="index-title">We'll be back in 2020</h1>
        <h2 class="index-subtitle subtitle"><span>Join us in Oslo on 14th and 15th May</span></h2>
        <Tickets />
      </section>
      <section class="simple-page">
        <h2>What happened to Web Rebels 2019?</h2>
        <p>Usually, after wrapping up the conference, we secure our venue for the following year straight away. This time however, we ran into an unexpected challenge: none of the dates available worked for us.</p>
        <p>We went looking for alternatives but ultimately, nothing fit what we were looking for. When you run a conference, you always work within certain constraints, and this time, we couldn’t make it work.</p>
        <p>As a consequence, there was no Web Rebels in 2019.</p>
        <p>The good news is that we have the dates and the venue we want for 2020.</p>
      </section>
      <div class="hero-image">
        <img src="https://2018.webrebels.org/static/webrebelBIG.759f990b.jpg" />
        <h1 class="hero-image-heading"><span>Class of Web Rebels 2020<br/>we love you!</span></h1>
      </div>
      <div class="video">
        <div class="iframe-wrapper">
          <iframe width="560" height="315" src="https://www.youtube.com/embed/Kq6vqdqku-U" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
      </div>
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
  margin: .5rem 0 4rem;
  width: $width-p;
  max-width: 66%;
  color: $color-white;
}
.index-title {
  font-size: 7rem;
  -webkit-text-stroke: $text-outline $color-main;
  text-stroke: $text-outline $color-main;
  color: transparent;
  max-width: 54rem;
  padding: 4rem 2rem 2rem;
  margin-bottom: 0;
  line-height: 1.05;
}
.index-subtitle {
  font-size: 1,4rem;
  font-weight: 400;
  text-transform: uppercase;

  color: $color-main;
  text-align: center;
  margin-bottom: 3rem;
  max-width: 20rem;
  padding: 0 1rem;
  line-height: 1.3;
}
.index-subtitle span {
  display: inline-block;
  position: relative;  
}
.index-subtitle span:before,
.index-subtitle span:after {
  content: "";
  position: absolute;
  height: 1px;
  border-bottom: $text-outline solid $color-main;
  top: 1.15em;
  width: 8rem;
  box-shadow: 0 0 .5em rgba(255, 255, 255, .5);
}
.index-subtitle span:before {
  right: 100%;
  margin-right: .1rem;
}
.index-subtitle span:after {
  left: 100%;
  margin-left: .1rem;
}

.hero {
  min-height: 66vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  .button {
    margin-bottom: 1rem;
  }
}
.hero-image {
  width: 100%;
  max-width: 1200px;
  margin: 5rem auto 10rem;
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
    font-size: 3rem;
    display: block;
    margin-bottom: 0;
    position: relative;
    top: -100%;
    z-index: 10;
    font-weight: 800;
    padding: .5rem .8rem .1rem;

    transform-origin: center;
    transform: rotateX(-2deg) rotateY(20deg);

    span {
      background: $color-main;
      color: $color-black;
      box-shadow: -.4rem 0 0 .4rem $color-main, .4rem 0 0 .4rem $color-main;
      transition: all .2s ease-in-out;
    }
  }
}

.video {
  width: $width-lead;
  margin: 5rem auto 10rem;
}
@media (max-width: $media-m) {
  .index-title {
    font-size: 4.5rem;
    border-top: none;
  }
}
@media (max-width: $media-s) {
  .index-title {
    font-size: 4.5rem;
    -webkit-text-stroke: $text-outline-s $color-main;
    text-stroke: $text-outline-s $color-main;
  }
  .index-subtitle {
    font-size: 1.3rem;
  }
  .index-subtitle span:before,
  .index-subtitle span:after {
    width: 6rem;
  }
  .intro {
    margin-bottom: 1rem;
  }
}

.light-theme {
  .intro {
    color: $color-black;
  }
  .index-title {
    -webkit-text-stroke: 0;
    text-stroke: 0;
    color: black;
  }
  .index-subtitle {
    color: $color-black;
  }
  .index-subtitle span:before,
  .index-subtitle span:after {
    border-bottom: $text-outline solid $color-black;
  }

  .hero-heading {
    span {
      background: $color-black;
      color: $color-main;
      box-shadow: -.4rem 0 0 .4rem $color-black, .4rem 0 0 .4rem $color-black;
    }
  }

  @media (max-width: $media-m) {
    .index-title {
      padding: 2.5rem 0 2rem;
      font-size: 5.5rem;
      border-top: none;
    }
  }
}
</style>
