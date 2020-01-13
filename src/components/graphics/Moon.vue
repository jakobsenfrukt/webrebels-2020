<template>
  <div class="graphic moon">
    <svg viewBox="0 0 14 14" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
        <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
            <path d="M5.32326309,3.57637938 C5.32326309,6.59528903 7.7705729,9.04259885 10.7894826,9.04259885 C12.1889803,9.04259885 12.9770075,7.91056569 13.684501,8.35579428 C14.5391579,10.3640276 11.0743237,13.7883047 7.50475345,13.7883047 C3.64961757,13.7883047 0.524412463,10.6630996 0.524412463,6.80796374 C0.524412463,3.19859967 3.37179868,-0.265803585 5.72634776,0.341004774 C6.09896225,0.887271565 5.32326309,2.14376863 5.32326309,3.57637938 Z" id="Path" fill="#FFFFFF"></path>
        </g>
    </svg>
  </div>
</template>

<style lang="scss" scoped>
@import '@/css/variables.scss';
.moon {
  width: .9rem;
  height: .9rem;
  display: inline-block;
  vertical-align: top;
  line-height: 1.6;

  svg {
    path {
      fill: $color-yellow;
    }
  }
}
</style>