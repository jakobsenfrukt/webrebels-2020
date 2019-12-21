<template>
  <a class="tickets button" href="#">
    <h1>Get tickets</h1>
  </a>
</template>

<style lang="scss" scoped>
@import '@/css/variables.scss';
.tickets {
  display: block;
  background: transparent;
  border: 3px solid $color-pink;
  color: $color-pink;
  width: $width-plus;
  max-width: 100%;
  margin: 1rem auto 2rem;
  padding: 1.2rem 1.5rem 1rem;

  &:hover {
    box-shadow: 0 0 10px $color-pink, inset 0 0 10px $color-pink;
    text-shadow: 0 0 5px $color-pink;
  }

  h1 {
    margin: 0;
    line-height: 1;
    font-size: 2rem;
    color: inherit;
    width: 100%;
  }

  @media screen and (prefers-color-scheme: light) {
    &:hover {
      box-shadow: 0 0 4px $color-pink, inset 0 0 4px $color-pink;
      text-shadow: 0 0 2px $color-pink;
    }
  }
  @media (max-width: $media-s) {
    width: 100%;

    h1 {
      font-size: 1.4rem;
    }
  }
}
.light-theme {
  .tickets:hover {
    box-shadow: 0 0 4px $color-pink, inset 0 0 4px $color-pink;
    text-shadow: 0 0 2px $color-pink;
  }
}
</style>
