<template>
  <div class="scroller">
    <div class="swiper-wrapper">
      <div class="swiper-slide">
        <slot>
        </slot>
      </div>
    </div>
    <div class="swiper-scrollbar"></div>
  </div>
</template>

<script>
import Swiper from 'swiper';

export default {
  mounted() {
    var swiper = new Swiper('.scroller', {
        scrollbar: '.swiper-scrollbar',
        direction: 'vertical',
        slidesPerView: 'auto',
        mousewheelControl: true,
        freeMode: true,
        freeModeMomentumBounce: false
    });
  },
};
</script>

<style lang="scss" scoped>
.scroller {
  height: 100%;
  width: 100%;
  position: relative;
  overflow: hidden;
}

.swiper-wrapper {
  height: 100%
}

.swiper-container {
  width: 100%;
  height: 100%;
}
.swiper-slide {
  font-size: 16px;
  height: auto;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  position: relative;
  flex-shrink: 0;
}

</style>
