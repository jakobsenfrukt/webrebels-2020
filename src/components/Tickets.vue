<template>
  <div>
    <a class="tickets button" href="#">
      <h1>Get tickets</h1>
      <p>
        Earlybird price!<br />
        happy times!
      </p>
      <p>
        info about tickets<br />
        price........5000kr
      </p>
    </a>
  </div>
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
  padding: 1.2rem 1.5rem 1rem;

  display: flex;
  justify-content: center;
  flex-wrap: wrap;

  &:hover {
    box-shadow: 0 0 10px $color-pink, inset 0 0 10px $color-pink;
    text-shadow: 0 0 5px $color-pink;
  }

  h1 {
    margin: 0;
    line-height: 1;
    font-size: inherit;
    color: inherit;
    width: 100%;
  }

  p {
    font-size: 1rem;
    margin: 2rem 0 0;
    text-align: left;
    text-transform: none;
    width: 50%;
    padding-right: 1.5rem;
    line-height: 1.2;
  }

  @media screen and (prefers-color-scheme: light) {
    &:hover {
      box-shadow: 0 0 4px $color-pink, inset 0 0 4px $color-pink;
      text-shadow: 0 0 2px $color-pink;
    }
  }
  @media (max-width: $media-s) {
    width: 100%;
    display: block;

    p {
      width: 100%;
    }
  }
}
</style>
