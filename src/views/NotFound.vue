<template>
  <div class="notfound">
    <main>
      <section>
        <div class="hero">
          <h1>404</h1>
          <p class="lead">
            Page not found! Just in case, are you sure you typed the URL correctly? In that case, there's probably something wrong on our end. Sorry about that!
            <br />
            <br />
            <a href="/">&rarr; Go to the front page</a>
          </p>
        </div>
      </section>
    </main>
  </div>
</template>

<script>

export default {
  name: 'notfound'
}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
h1 {
  font-size: 7rem;
  color: $color-red;
  font-family: $monospace;
  letter-spacing: 2px;
}
</style>