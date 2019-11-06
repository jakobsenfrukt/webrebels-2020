<template>
  <section class="speakers index">
    <h2 class="speakers-heading">Speakers</h2>
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
    <router-link to="/speakers" class="view-all button">Show all speakers</router-link>
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
    font-size: 2rem;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 2rem;
  }
}
.speaker-list {
  display: flex;
  justify-content: flex-start;
  align-items: flex-start;
  flex-wrap: wrap;
}
.speaker {
  color: inherit;
  width: 33.333333%;
  margin: 0 auto 2rem 0;
  position: relative;
  padding: 1rem;

  &-image {
    padding: 1rem;
    img {
      border-radius: 50%;
    }
    &_fallback {
      background: $color-main;
      width: 100%;
      padding-top: 100%;
      border-radius: 50%;
    }
  }
  &-name {
    font-size: 1.8rem;
    margin-bottom: 0;
    text-align: center;
    margin: -4rem auto 1.4rem;
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
    margin-bottom: 1rem;
    font-family: $monospace;
    line-height: 1.3rem;
    text-align: center;
  }
}
</style>
