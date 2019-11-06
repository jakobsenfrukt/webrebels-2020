<template>
  <main class="speakers">
    <h1 class="page-title">Speakers</h1>
    <p class="lead">As usual we have a bunch of cool speakers joining us from all over the world!</p> 
    <Tickets />
    <div class="speaker-list">
      <div v-for="(speaker, index) in speakers" :key="index" :id="speaker.id" class="speaker">
        <div class="speaker-image">
          <img v-if="speaker.image" :src="speaker.image" />
          <div v-else class="speaker-image_fallback"></div>
        </div>
        <div class="speaker-text">
          <h3 class="speaker-name">{{ speaker.name }}</h3>
          <p class="speaker-title">{{ speaker.title }}</p>
          <p class="speaker-bio">{{ speaker.bio }}</p>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import speakers from '@/data/speakers.json'
import Tickets from '@/components/Tickets.vue'

export default {
  components: {
    Tickets
  },
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
  margin: 5rem 0;
}
.speaker {
  display: flex;
  color: inherit;
  max-width: 50rem;
  margin: 0 auto 2rem 0;

  &-image {
    width: 30%;
    padding-right: 2rem;

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
  &-text {
    width: 70%;
  }
  &-name {
    font-size: 3rem;
    margin-bottom: 0;
  }
  &-title {
    margin-bottom: 1rem;
    font-family: $monospace;
  }

  /*&:nth-child(even) {
    margin: 0 0 2rem auto;
    .speaker-image {
      order: 2;
    }
    .speaker-text {
      order: 1;
    }
  }*/
}
</style>
