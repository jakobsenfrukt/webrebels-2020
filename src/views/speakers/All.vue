<template>
  <main class="speakers">
    <div class="hero">
      <h1 class="page-title">Speakers</h1>
      <p class="lead">As usual we have a bunch of cool speakers joining us from all over the world!</p> 
      <Tickets />
    </div>
    <div class="speaker-list">
      <div v-for="(speaker, index) in speakers" :key="index" :id="speaker.id" class="speaker">
        <div class="speaker-image">
          <img v-if="speaker.image" :src="speaker.image" />
          <div v-else class="speaker-image_fallback"></div>
        </div>
        <div class="speaker-text">
          <a class="schedule-time" href="/schedule">Monday 14th May at 10:30</a>
          <h3 class="speaker-name">{{ speaker.name }}</h3>
          <p class="speaker-title">{{ speaker.title }}</p>
          <p class="speaker-bio">{{ speaker.bio }}</p>
          <p class="speaker-some">
            <span class="some-item">Twitter: <a href="#">@juanpablo</a></span>
            <span class="some-item">Github: <a href="#">@juanpablo</a></span>
            <span class="some-item">Website: <a href="#">juanpabloboi.com</a></span>
          </p>
        </div>
        <div class="read-more" :class="{ open: open }" @click="open = !open">
          <div class="header">
            <span class="suptitle">Juan Pablo will talk about</span>
            <h3 class="talk-title">DevTools for the Progressive Web</h3>
          </div>
          <div class="content">
            <p>Usually, after wrapping up the conference, we secure our venue for the following year straight away. This time however, we ran into an unexpected challenge: none of the dates available worked for us.</p>
            <p>We went looking for alternatives but ultimately, nothing fit what we were looking for. When you run a conference, you always work within certain constraints, and this time, we couldn’t make it work.</p>
            <p>As a consequence, there will be no Web Rebels in 2019. You may have guessed this already.</p>
            <p>The good news is that we have the dates and the venue we want for 2020.</p>
          </div>
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
      speakers,
      open: false
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
  flex-wrap: wrap;
  color: inherit;
  max-width: 50rem;
  margin: 0 auto 6rem;
  padding-top: 5rem;
  &:first-child {
    padding-top: 0;
  }

  &-image {
    width: 30%;
    padding-right: 2rem;

    img {
      border-radius: 50%;
    }

    &_fallback {
      background: $color-teal;
      width: 100%;
      padding-top: 100%;
      border-radius: 50%;
    }
  }
  &-text {
    width: 70%;
    p {
      margin-left: 0;
    }
  }
  &-name {
    font-size: 2.8rem;
    margin-bottom: 0;
    text-align: left;
  }
  &-title {
    margin-bottom: 1rem;
    font-family: $monospace;
  }

  &-some {
    font-family: $monospace;
    font-size: $font-s;

    .some-item {
      display: inline-block;
      margin-right: 1rem;
    }
  }

  .schedule-time {
    text-transform: uppercase;
    font-family: $monospace;
    display: inline-block;
    color: $color-main;
    background: $color-black;
    padding: .2rem .8rem 0;
    margin-bottom: 1rem;

    &:hover {
      color: $color-pink;
    }
  }

  .read-more {
    width: 100%;
    color: $color-white;
    padding-top: 2rem;
    order: 3 !important;

    .content {
      display: none;
    }
    &.open {
      .content {
       display: block;
      }

      .talk-title {
        &:after {
          content: "×";
        }
      }
    }
  }
  .header {
    transition: all .2s ease-in-out;
    margin-bottom: 1.5rem;
    cursor: pointer;
    &:after {
      content: " ";
      display: block;
      width: 100%;
      height: 2px;
      background: $color-pink;
    }
    &:hover {
      color: $color-pink;
      text-shadow: 0 0 5px $color-pink;
      &:after {
        box-shadow: 0 0 10px $color-pink;
      }
      .talk-title {
        color: $color-white;
      }
    }
  }
  .suptitle {
    font-family: $monospace;
    display: block;
    margin-bottom: .5rem;
    color: $color-pink;
  }

  .talk-title {
    text-align: left;
    font-size: 1.8rem;
    color: $color-white;

    &:after {
      content: "↓";
      font-family: $monospace;
      float: right;
    }
  }
}

@media screen and (prefers-color-scheme: light) {
  .speaker {
    .schedule-time {
      background: $color-yellow;
      color: $color-black;
    }
    .read-more {
      color: $color-black;
      border-color: $color-pink;
    }
    .header {
      &:hover {
        text-shadow: 0 0 2px $color-pink;
        &:after {
          box-shadow: 0 0 5px $color-pink;
        }
        .talk-title {
          color: $color-black;
        }
      }
    }
    .suptitle {
      color: $color-pink;
    }

    .talk-title {
      color: $color-black;
    }

    &-some {
      .some-item a {
        color: $color-blue;
      }
    }
  }
}

@media (max-width: $media-m) {
  .speaker {
    .speaker-image {
      order: 2;
      width: 50%;
      padding-right: 0;
      padding-left: 2rem;
    }
    .speaker-text {
      order: 1;
      width: 50%;
    }
  }
}

@media (max-width: $media-s) {
  .speaker {
    display: block;
    padding: 0 1rem;
    text-align: center;
    .speaker-image {
      width: 60%;
      margin: 0 auto -1.5rem;
      padding: 0;
    }
    .speaker-text {
      width: 100%;
    }
    .schedule-time, .speaker-name, .speaker-title {
      text-align: center;
      margin-left: auto;
      margin-right: auto;
    }
    .speaker-name {
      font-size: 2rem;
    }
    .talk-title {
      font-size: 1.5rem;
      text-align: center;
      &:after {
        display: block;
        float: none;
        margin-top: .5rem;
      }
    }
    p {
      text-align: left;
      margin: 0 auto 1.5rem;
    }
    .read-more .content p {
      width: 90%;
    }
  }
}

@media (min-width: $media-m) {
  .speaker {
    &:nth-child(even) {
      .speaker-image {
        order: 2;
      }
      .speaker-text {
        order: 1;
      }
    }
  }
}
</style>
