<template>
  <div class="newsletter">
    <h2>Sign up to our newsletter</h2>
    <input type="text" />
  </div>
</template>

<style lang="scss" scoped>
@import '@/css/variables.scss';
.newsletter {
  background: $color-orange;
  padding: 1rem 1.8rem;

  input {
    display: block;
    font-size: 1rem;
    font-family: $sans-serif;
    line-height: 1.5;
    width: 20rem;
    margin: 1rem auto;
    padding: .5rem 1rem;
  }
}
</style>
