<template>
  <div class="mainSlider">
    <div v-swiper:mySwiper="swiperOption">
      <div class="swiper-wrapper">
        <div class="swiper-slide us1 us">
          <p class="introWordSmall animated fadeInUp delay1">奢华 | 之美</p>
          <p class="introWordBig animated fadeInUp delay2">无与伦比 一 享受</p>
        </div>
        <div class="swiper-slide us2 us">
          <p class="introWordSmall animated fadeInUp delay1">奢华 | 之美</p>
          <p class="introWordBig animated fadeInUp delay2">无与伦比 一 享受</p>
        </div>
        <div class="swiper-slide us3 us">
          <p class="introWordSmall animated fadeInUp delay1">奢华 | 之美</p>
          <p class="introWordBig animated fadeInUp delay2">无与伦比 一 享受</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "mainSlider",

  data() {
    return {
      swiperOption: {
        grabCursor: true,
        loop: true,
        speed: 700,
        autoplay: {
          delay: 5000
        }
      }
    };
  }
};
</script>
<style lang="scss" scoped>
.mainSlider {
  position: relative;
}
.us {
  width: 100vw;
  height: 90vh;
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  .introWordSmall {
    font-weight: 100;
    font-size: 1.5rem;
    @media screen and (max-width: 1000px) {
      font-size: 1.25rem;
    }
    @media screen and (max-width: 500px) {
      font-size: 1rem;
    }
  }
  .introWordBig {
    font-weight: bolder;
    font-size: 6rem;
    @media screen and (max-width: 1000px) {
      font-size: 4.5rem;
    }
    @media screen and (max-width: 500px) {
      font-size: 3rem;
    }
  }
  p {
    z-index: 4;
    margin: 0.5rem;
  }
}
.us::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(1, 1, 1, 0.25);
}
.us3::after {
  background: rgba(1, 1, 1, 0.4);
}
.delay1 {
  animation-delay: 1s;
}
.delay2 {
  animation-delay: 2s;
}
.us1 {
  background-image: url("../assets/image/house.jpg");
}
.us2 {
  background-image: url("../assets/image/boat.jpg");
}
.us3 {
  background-image: url("../assets/image/car.jpg");
}
</style>
