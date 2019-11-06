<template>
  <footer class="site-footer">
    <section class="some">
      REMEMBER TO FIND, FOLLOW, TRACK, LIKE &amp; LOVE US ELSEWHERE
      <a href="https://twitter.com/web_rebels">Twitter</a>
      <a href="https://www.youtube.com/channel/UCM9cTs_C0PmTlHXTNrqTpnw">YouTube</a>
    </section>
    <nav class="footer-nav">
      <div class="previous-years">
        <p>Check out previous years:</p>
        <a href="https://2012.webrebels.org/">2012</a>
        <a href="https://2013.webrebels.org/">2013</a>
        <a href="https://2014.webrebels.org/">2014</a>
        <a href="https://2015.webrebels.org/">2015</a>
        <a href="https://2016.webrebels.org/">2016</a>
        <a href="https://2017.webrebels.org/">2017</a>
        <a href="https://2018.webrebels.org/">2018</a>
      </div>
      <div>
        <a href="#" class="to-top">&uarr; To top</a>
      </div>
    </nav>
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

  @media (max-width: $media-s) {
    padding:  3rem 1rem 1rem;
  }

  p {
    max-width: none;
  }
}
.footer-nav {
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
  z-index: 1000;
  display: flex;
  justify-content: space-between;
  font-family: $monospace;
  padding: .25rem 1rem;
  background: $color-black;

  p {
    margin: 0;
    display: inline-block;
    margin-right: 1rem;
  }

  a {
    display: inline-block;
    margin-right: 1rem;
    text-align: center;
    color: $color-yellow;
  }

  .to-top {
    color: $color-white;
  }
}
</style>
