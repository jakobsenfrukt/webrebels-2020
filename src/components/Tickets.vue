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
  margin: 1rem auto 6rem;
  font-size: 2rem;
  padding: .6em 1em .36em;

  &:hover {
    box-shadow: 0 0 10px $color-pink, inset 0 0 10px $color-pink;
    text-shadow: 0 0 5px $color-pink;
  }

  h1 {
    margin: 0;
    line-height: 1;
    font-size: inherit;
    color: inherit;
  }

  @media screen and (prefers-color-scheme: light) {
    &:hover {
      box-shadow: 0 0 4px $color-pink, inset 0 0 4px $color-pink;
      text-shadow: 0 0 2px $color-pink;
    }
  }
}
</style>
