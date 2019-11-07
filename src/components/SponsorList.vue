<template>
  <section class="friends index">
    <h2 class="friends-heading">Sponsors</h2>
    <div class="friend-list">
      <a href="#" class="friend">
        <img class="friend-logo" src="https://2017.webrebels.org/files/acando.svg" />
      </a>
            <a href="#" class="friend">
        <img class="friend-logo color" src="https://2017.webrebels.org/files/finn.svg" />
      </a>
      <a href="#" class="friend">
        <img class="friend-logo color" src="https://2017.webrebels.org/files/google.svg" />
      </a>
      <a href="#" class="friend">
        <img class="friend-logo" src="https://2017.webrebels.org/files/bekk.svg" />
      </a>
      <a href="#" class="friend">
        <img class="friend-logo" src="https://2017.webrebels.org/files/acando.svg" />
      </a>
      <a href="#" class="friend">
        <img class="friend-logo" src="https://2017.webrebels.org/files/acando.svg" />
      </a>
    </div>
    <router-link to="/sponsors" class="button">Become a sponsor of Web Rebels 2020</router-link>
  </section>
</template>

<style lang="scss" scoped>
@import '@/css/variables.scss';
.friends {
  &-heading {
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 2rem;
  }
}
.friend-list {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-wrap: wrap;
}
.friend {
  display: block;
  color: inherit;
  width: 20%;
  margin: 0;
  position: relative;
  padding: 1rem;
  text-align: center;

  @media (min-width: $media-l) {
    width: 15%;
  }
  @media (max-width: $media-m) {
    width: 25%;
  }
  @media (max-width: $media-s) {
    width: 33.333333%;
  }

  &-logo {
    display: block;
    width: 100%;
    height: auto;
    filter: grayscale(100%) invert(100%);
    &.color {
      filter: none;
    }
  }
}

@media screen and (prefers-color-scheme: light) {
  .friend-logo {
    filter: none;
  }
}
</style>
