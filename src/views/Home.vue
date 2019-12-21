<template>
  <div class="home">
    <main>
      <p class="intro"><a href="/about">Web Rebels</a> is a non-profit community conference for anyone who loves developing applications and services using web technology. Two days, one track, 16 speakers.</p>
      <section class="hero">
        <h1 class="index-title">We'll be back in 2020</h1>
        <h2 class="index-subtitle subtitle"><span>Join us in Oslo on 14th and 15th May</span></h2>
        <Tickets />
      </section>
      <!--<div class="hero-image">
        <img src="https://2018.webrebels.org/static/webrebelBIG.759f990b.jpg" />
        <h1 class="hero-image-heading"><span class="heading-top">Class of Web Rebels 2020</span><span class="heading-bottom">we love you!</span></h1>
      </div>-->
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
  border-top: $text-outline solid $color-main;
  padding: 4rem 2rem 2rem;
  margin-bottom: 0;
}
.index-subtitle {
  font-size: 1,4rem;
  font-weight: 400;
  text-transform: uppercase;

  color: $color-main;
  text-align: center;
  margin-bottom: 3rem;
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
  top: .25em;
  width: 7rem;
}
.index-subtitle span:before {
  right: 100%;
  margin-right: 15px;
}
.index-subtitle span:after {
  left: 100%;
  margin-left: 15px;
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
@media (max-width: $media-m) {
  .index-title {
    padding: 2.5rem 0 2rem;
    font-size: 5.5rem;
    border-top: none;
  }
  .index-subtitle span:before,
  .index-subtitle span:after {
    border-bottom: none;
  }
}
@media (max-width: $media-s) {
  .index-title {
    font-size: 4.5rem;
    padding: 2.5rem 0 2rem;
    -webkit-text-stroke: $text-outline-s $color-main;
    text-stroke: $text-outline-s $color-main;
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
    border-top: $text-outline solid $color-black;
  }
  .index-subtitle {
    color: $color-black;
  }
  .index-subtitle span:before,
  .index-subtitle span:after {
    border-bottom: $text-outline solid $color-black;
  }

  @media (max-width: $media-m) {
    .index-title {
      padding: 2.5rem 0 2rem;
      font-size: 5.5rem;
      border-top: none;
    }
    .index-subtitle span:before,
    .index-subtitle span:after {
      border-bottom: none;
    }
  }
}
</style>
