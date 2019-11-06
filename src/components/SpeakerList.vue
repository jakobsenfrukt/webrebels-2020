<template>
  <section class="speakers index">
    <h2 class="speakers-heading">Speakers</h2>
    <p class="lead">We’re putting the same effort and love into the conference and its line-up that you are used to from previous years.</p>
    <div class="speaker-list">
      <a v-for="(speaker, index) in speakers.slice(0,9)" :key="index" :href="`/speakers/#${speaker.id}`" class="speaker">
        <div class="speaker-image">
          <img v-if="speaker.image" :src="speaker.image" />
          <div v-else class="speaker-image_fallback"></div>
        </div>
        <h3 class="speaker-name">{{ speaker.name }}</h3>
        <div class="speaker-text">
          <p class="speaker-title">{{ speaker.title }}</p>
        </div>
      </a>
    </div>
    <router-link to="/speakers" class="view-all button">All speakers</router-link>
    <router-link to="/speakers" class="view-schedule button">View schedule</router-link>
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
.speakers {
  &-heading {
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 2rem;
  }
}
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
      box-shadow: 0 0 12px $color-yellow;
    }
  }

  &-image {
    padding: 1rem;
    img {
      border-radius: 50%;
      transition: all 0.2s ease-in-out;
    }
    &_fallback {
      background: $color-yellow;
      width: 100%;
      padding-top: 100%;
      border-radius: 50%;
      transition: all 0.2s ease-in-out;
    }
  }
  &-name {
    display: inline-block;
    font-size: 1.8rem;
    margin-bottom: 0;
    position: relative;
    top: -5rem;
    background: $color-main;
    color: black;
    padding: .4rem .8rem;

    transform-origin: center;
    transform: rotate(-5deg);
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
</style>
