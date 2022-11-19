<template>
  <Swiper
    :navigation="true"
    :modules="modules"
    class="main__slider-wrapper"
    :slides-per-view="3"
    :space-between="20"
  >
    <SwiperSlide
      v-for="slide in slider"
      :key="slide.id"
      class="main__slider-slide"
    >
      <!-- <img
        :src="require(`@/assets/img/${slide.img}.jpg`)"
        class="main__slider-slide-img"
      /> -->
      <div class="main__slider-info">
        <span class="main__slider-slide-title">{{ slide.title }}</span>
        <div class="main__slider-slider-subinfo">
          <div class="main__slider-slider-time">{{ slide.time }}</div>
          <div class="main__slider-slider-peoples">{{ slide.count }}</div>
          <div class="main__slider-slider-cost">₽ {{ slide.price }}</div>
        </div>
      </div>
    </SwiperSlide>
  </Swiper>
</template>

<script>
  import { Swiper, SwiperSlide } from "swiper/vue";
  import { Navigation } from "swiper";
  import "swiper/css";
  import "swiper/css/navigation";

  export default {
    components: {
      Swiper,
      SwiperSlide,
    },
    data() {
      return {
        modules: [Navigation],
      };
    },
    props: {
      slider: {
        type: Array,
        default: () => [],
      },
    },
    methods: {
      getImgUrl(pic) {
        return require("../assets/" + pic);
      },
    },
  };
</script>

<style scoped>
  .main__slider-slide {
    position: relative;
    width: 100%;
    height: 294px;

    overflow: hidden;
    background-color: gray;
    border-radius: 12px;
  }
  .main__slider-slide-img {
    position: absolute;
    top: 0;
    left: 0;
    max-width: 100%;
    max-height: 100%;
    width: 100%;
    height: 100%;
  }
  .main__slider-info {
    width: 100%;
    height: 100%;
    position: absolute;
    bottom: 0;
    padding: 24px;

    display: flex;
    flex-direction: column;
    justify-content: flex-end;

    background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
  }
  .main__slider-slide-title {
    font-weight: 700;
    font-size: 25px;
    line-height: 30px;

    padding-bottom: 16px;
    color: white;
  }
  .main__slider-slider-subinfo {
    width: 100%;
    display: flex;
    flex-direction: row;
    gap: 30px;
  }
  .main__slider-slider-time {
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 21px;

    color: #ffffff;
  }
  .main__slider-slider-peoples {
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 21px;

    color: #ffffff;
  }
  .main__slider-slider-cost {
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 21px;

    color: #ffffff;
  }
</style>

<style>
  .swiper-button-prev,
  .swiper-button-next {
    width: auto;
  }
  .swiper-button-prev::after {
    width: 44px;
    height: 44px;
    font-family: "SF Pro Display", sans-serif;
    content: "";
    background-image: url(~/assets/img/icon/left.svg);
  }
  .swiper-button-next::after {
    width: 44px;
    height: 44px;
    font-family: "SF Pro Display", sans-serif;
    content: "";
    background-image: url(~/assets/img/icon/right.svg);
  }
</style>
