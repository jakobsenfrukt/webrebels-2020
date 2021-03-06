<template>
  <section class="speakers index">
    <h2 class="section-heading speakers-heading">Speakers</h2>
    <p class="lead">We’re putting the same effort and love into the conference and its line-up that you are used to from previous years.</p>
    <div class="speaker-list">
      <a v-for="(speaker, index) in speakers.slice(0,9)" :key="index" :href="`/speakers/#${speaker.id}`" class="speaker">
        <div class="speaker-image">
          <img v-if="speaker.image" :src="speaker.image" />
          <div v-else class="speaker-image_fallback"></div>
        </div>
        <h3 class="speaker-name"><span>{{ speaker.name }}</span></h3>
        <div class="speaker-text">
          <p class="speaker-title">{{ speaker.title }}</p>
        </div>
      </a>
    </div>
    <div class="buttonbox">
      <router-link to="/speakers" class="view-all button">All speakers</router-link>
      <router-link to="/speakers" class="view-schedule button">View schedule</router-link>
    </div>
  </section>
</template>

<script>
import speakers from '@/data/speakers.json'

export default {
  data: function() {
    return {
      speakers
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/css/variables.scss';
.speaker-list {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-wrap: wrap;
}
.speaker {
  color: inherit;
  width: 33.333333%;
  margin: 0;
  position: relative;
  padding: 1rem;
  text-align: center;

  @media (min-width: $media-l) {
    width: 25%;
  }
  @media (max-width: $media-m) {
    width: 50%;
  }
  @media (max-width: $media-s) {
    width: 100%;
  }

  &:hover {
    .speaker-image img, .speaker-image_fallback {
      box-shadow: 0 0 .8rem rgba(255, 255, 255, .3);
    }
    .speaker-name span {
      color: $color-white;
    }
  }

  &-image {
    padding: 1rem;
    max-width: 20rem;
    margin: 0 auto;
    img {
      border-radius: 50%;
      transition: all 0.2s ease-in-out;
    }
    &_fallback {
      background: $color-teal;
      width: 100%;
      padding-top: 100%;
      border-radius: 50%;
      transition: all 0.2s ease-in-out;
    }
  }
  &-name {
    font-size: 2.1rem;
    margin-bottom: 0;
    position: relative;
    top: -4rem;
    z-index: 10;
    font-weight: 800;
    padding: .5rem .8rem .1rem;
    line-height: 1.56;

    transform-origin: center;
    transform: rotateX(-2deg) rotateY(20deg);

    span {
      background: $color-black;
      color: $color-main;
      box-shadow: -.4rem 0 0 .4rem $color-black, .4rem 0 0 .4rem $color-black;
      transition: all .2s ease-in-out;
    }
  }
  &-text {
    width: 80%;
    margin: auto;
  }
  &-title {
    margin: -3rem auto 0;
    font-family: $monospace;
    line-height: 1.3rem;
    text-align: center;
  }
}
.speaker:nth-child(odd) {
  perspective: 1200px;
  .speaker-name {
    transform: rotateX(20deg) rotateY(-20deg);
  }
}
.speaker:nth-child(even) {
  perspective: -1200px;
  .speaker-name {
    transform: rotateX(-2deg) rotateY(20deg);
  }
}
.speaker:nth-child(1n+3) {
  perspective: 1200px;
  .speaker-name {
    transform: rotateX(8deg) rotateY(20deg);
  }
}
.buttonbox {
  display: flex;
  max-width: $width-lead;
  margin: 2rem auto;

  .button {
    margin: .5rem .5rem;
  }
}
.light-theme {
  .speaker-name {
    span {
      background: $color-main;
      color: $color-black;
      box-shadow: -.4rem 0 0 .4rem $color-main, .4rem 0 0 .4rem $color-main;
    }
  }
  .speaker:hover .speaker-name span {
    color: $color-teal;
  }
}
</style>
