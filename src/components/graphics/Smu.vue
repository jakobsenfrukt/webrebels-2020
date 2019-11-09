<template>
  <div id="smu" class="smu" @mouseover="smile = true" @mouseout="smile = false">
    <svg class="default" viewBox="0 0 117 166" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
      <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
        <g transform="translate(2.862421, 0.223604)">
          <path d="M94.3136,70.6541 C103.6786,81.6941 113.6706,102.0331 110.5316,120.8711 C105.7136,147.8181 76.3816,161.4671 59.3916,162.2401 C42.4016,163.0151 27.9426,162.0441 10.1926,143.0081 C-7.5564,123.9721 2.4726,83.7821 12.8216,71.3951 C23.1706,59.0081 39.2716,50.5661 56.6776,52.6471 C74.0846,54.7281 86.6326,61.5981 94.3136,70.6541 Z" class="fill stroke body"></path>
          <g v-if="smile">
            <path d="M75.9073,114.9061 C75.9073,114.9061 69.3863,132.3491 53.9443,132.3491 C38.5023,132.3491 31.9803,114.9061 31.9803,114.9061 C31.9803,114.9061 43.9703,117.2581 53.9443,117.2581 C63.9193,117.2581 75.9073,114.9061 75.9073,114.9061 Z" stroke-linecap="round" stroke-linejoin="round" class="stroke fill-light"></path>
          </g>
          <g v-else>
            <path d="M32.5118,115.9061 C32.5118,115.9061 38.0328,122.3491 53.4748,122.3491 C68.9168,122.3491 74.4378,115.9061 74.4378,115.9061" stroke-linecap="round" stroke-linejoin="round" class="stroke mouth"></path>
          </g>
          <g v-if="eyesOpen">
            <path d="M28.5821,95.9876 C28.5821,93.0116 26.1701,90.5996 23.1941,90.5996 C20.2191,90.5996 17.8071,93.0116 17.8071,95.9876 C17.8071,98.9636 20.2191,101.3756 23.1941,101.3756 C26.1701,101.3756 28.5821,98.9636 28.5821,95.9876" class="stroke-thin fill-dark eyes-open"></path>
            <path d="M89.0811,95.9876 C89.0811,93.0116 86.6691,90.5996 83.6931,90.5996 C80.7181,90.5996 78.3061,93.0116 78.3061,95.9876 C78.3061,98.9636 80.7181,101.3756 83.6931,101.3756 C86.6691,101.3756 89.0811,98.9636 89.0811,95.9876" class="stroke-thin fill-dark eyes-open"></path>
          </g>
          <g v-else>
            <path d="M17.7452,96.8177 C17.7452,96.8177 19.9842,94.4297 23.1332,94.4297 C26.2822,94.4297 28.5212,96.8177 28.5212,96.8177" stroke-linecap="round" class="stroke-medium eyes"></path>
            <path d="M78.2452,96.8177 C78.2452,96.8177 80.4832,94.4297 83.6332,94.4297 C86.7812,94.4297 89.0202,96.8177 89.0202,96.8177" stroke-linecap="round" class="stroke-medium eyes"></path>
          </g>
        </g>
      </g>
    </svg>
    <div class="menu">
      <span class="action good">Feed</span>
      <span class="action">Pet</span>
      <span class="action evil">Kick</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Smu',
  data: function() {
    return {
      eyesOpen: true,
      smile: false
    }
  },
  methods: {
    blink: function() {
      let seconds;
      this.eyesOpen = !this.eyesOpen;
      if (this.eyesOpen) {
        seconds = Math.floor(Math.random() * 3600) + 1800
      } else {
        seconds = 200
      }
      setTimeout(this.blink, seconds)
    }
  },
  created() {
    this.blink()
  }
}
</script>

<style lang="scss" scoped>
@import '@/css/variables.scss';
.smu {
  cursor: pointer;
  position: fixed;
  bottom: 1.444rem;
  left: 1.444rem;
  width: 60px;
  z-index: 9999;
}

svg {
  width: 100%;

  > * {
    transition: all .3s ease-in-out;
  }
}
.fill {
  fill: $color-yellow;

  &-light {
    fill: $color-yellow;
  }
  &-dark {
    fill: $color-black;
  }
}
.stroke {
  stroke-width: 6;
  stroke: $color-black;

  &-thin {
    stroke-width: 2;
    stroke: $color-black;
  }

  &-medium {
    stroke-width: 4;
    stroke: $color-black;
  }

  &.body {
    stroke-width: 7;
    stroke: $color-black;
  }
}
.menu {
  position: absolute;
  top: 0;
  left: 70%;

  .action {
    display: inline-block;
    background: black;
    color: $color-white;
    font-size: $font-s;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: 600;
    padding: 2px 4px;
    border-radius: 3px;
    &:hover {
      color: $color-yellow;
      font-weight: 900;
      cursor: pointer;
    }
    &.evil {
      &:hover {
        color: $color-red;
      }
    }
    &.good {
      &:hover {
        color: $color-green;
      }
    }
    &:nth-child(1) {
      transform: rotate(-30deg) translate(1rem, -.5rem);
    }
    &:nth-child(2) {
      transform: rotate(-20deg) translateX(2rem);
    }
    &:nth-child(3) {
      transform: rotate(-10deg) translateX(2.3rem);
    }
    &:nth-child(4) {
      transform: rotate(5deg) translateX(2.3rem);
    }
  }
}
</style>