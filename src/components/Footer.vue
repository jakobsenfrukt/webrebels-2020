<template>
  <footer class="site-footer">
    <a href="#" class="to-top">To top</a>
    <div class="previous-years">
      <a href="#">2018</a>
      <a href="#">2017</a>
      <a href="#">2016</a>
      <a href="#">2015</a>
      <a href="#">2014</a>
      <a href="#">2013</a>
      <a href="#">2012</a>
    </div>
  </footer>
</template>

<script>
export default {
  props: {
    text: String
  }
}
</script>

<style scoped lang="scss">
@import '@/css/variables.scss';
.site-footer {
  padding: 6rem 3rem 12rem;
  position: relative;

  @media (max-width: $sm) {
    padding:  3rem 1rem 1rem;
  }

  p {
    max-width: none;
  }
}
.to-top {
  color: inherit;
}
</style>
