<template>
  <Swiper class="main__slider-wrapper" :slides-per-view="3" :space-between="20">
    <SwiperSlide class="main__slider-slide">
      <img
        src="~/assets/img/slide1.jpg"
        alt=""
        class="main__slider-slide-img"
      />
      <div class="main__slider-info">
        <span class="main__slider-slide-title"
          >Путешествие к Эльбрусу и озеру Гижгит</span
        >
        <div class="main__slider-slider-subinfo">
          <div class="main__slider-slider-time">12 часов</div>
          <div class="main__slider-slider-peoples">12 чел</div>
          <div class="main__slider-slider-cost">₽ 20 000</div>
        </div>
      </div>
    </SwiperSlide>
    <SwiperSlide class="main__slider-slide">Slide 2</SwiperSlide>
    <SwiperSlide class="main__slider-slide">Slide 3</SwiperSlide>
    <SwiperSlide class="main__slider-slide">Slide 4</SwiperSlide>
    <SwiperSlide class="main__slider-slide">Slide 5</SwiperSlide>
  </Swiper>
</template>

<script>
  import { Swiper, SwiperSlide } from "swiper/vue";
  import "swiper/css";

  export default {
    components: {
      Swiper,
      SwiperSlide,
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
