<template>
  <div class="newsletter" :class="{ closed: closed }">
    <h2 class="section-heading">Sign up to our newsletter</h2>
    <!-- Begin Mailchimp Signup Form -->
    <div id="mc_embed_signup">
      <form action="https://webrebels.us3.list-manage.com/subscribe/post?u=f515e6756e5ffeffd7a28a60d&amp;id=7d5e649dbe" method="post" id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
        <div id="mc_embed_signup_scroll">
          <div class="mc-field-group">
            <label for="mce-EMAIL">Email</label>
            <input type="email" value="" name="EMAIL" class="required email" id="mce-EMAIL" placeholder="hi@example.pizza">
          </div>
          <div id="mce-responses" class="clear">
            <div class="response" id="mce-error-response" style="display:none"></div>
            <div class="response" id="mce-success-response" style="display:none"></div>
          </div>
          <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
          <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_f515e6756e5ffeffd7a28a60d_7d5e649dbe" tabindex="-1" value=""></div>
          <input type="submit" value="Subscribe" name="subscribe" id="mc-embedded-subscribe" class="button">
        </div>
      </form>
    </div>
    <!--End mc_embed_signup-->
    <div class="close" @click="closed = !closed">&times;</div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      closed: false
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/css/variables.scss';
.newsletter {
  background: transparent;
  box-shadow: 0 0 0 2px $color-main;
  padding: 3rem 3rem;
  width: $width-lead;
  max-width: 100%;
  margin: 2rem auto 4rem;
  position: relative;
  color: $color-main;

  .close {
    display: block;
    position: absolute;
    top: .5rem;
    right: .5rem;
    font-size: 2rem;
    line-height: 1;
    cursor: pointer;
  }

  &.closed {
    visibility: hidden;
  }

  h2 {
    font-size: 2rem;
  }

  input {
    display: block;
    font-size: 1rem;
    font-family: $sans-serif;
    line-height: 1.5;
    width: 20rem;
    margin: 1rem auto;
    padding: .5rem 1rem;
    border: none;
  }
}
.mc-field-group {
  width: 100%;
  margin: 0 auto;

  label {
    font-family: $monospace;
    margin: 0;
  }
  .email {
    width: 100%;
    margin: 0;
    padding: 1rem;
    border: none;
    font-family: $monospace;

    &:hover, &:focus {
      box-shadow: 0 0 10px $color-main;
      outline: none;
    }
  }
}
#mc-embedded-subscribe {
  font-family: $monospace;
  width: 100%;
  margin: 1rem auto;
  cursor: pointer;
}
@media (max-width: $media-s) {
  .newsletter {
    width: 94%;
  }
}
.light-theme {
  .newsletter {
    background: transparent;
    box-shadow: 0 0 0 2px $color-black;
    color: $color-black;
  }
  .mc-field-group {
    .email {
      border: 2px solid $color-black;
    }
  }
}
</style>
