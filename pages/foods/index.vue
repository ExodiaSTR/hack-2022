<template>
  <div class="tours">
    <div class="container">
      <NuxtLink :to="link" class="tours__back">Назад на главную</NuxtLink>
      <div class="tours__title">Национальные блюда</div>
      <div class="tours__subtitle">
        Мы вам покажем национальные блюда Дагестана!
      </div>
      <div class="tours-content">
        <div class="main__slider">
          <Swiper
            :modules="modules"
            class="main__slider-wrapper"
            :slides-per-view="3"
            :space-between="20"
          >
            <SwiperSlide
              class="main__slider-slide"
              @click="$router.push('/tours/1/')"
            >
              <img src="@/assets/img/eda1.jpg" class="main__slider-slide-img" />
              <div class="main__slider-info">
                <span class="main__slider-slide-title">Чуду</span>
              </div>
            </SwiperSlide>
            <SwiperSlide
              class="main__slider-slide"
              @click="$router.push('/tours/1/')"
            >
              <img src="@/assets/img/eda2.jpg" class="main__slider-slide-img" />
              <div class="main__slider-info">
                <span class="main__slider-slide-title">Аварский хинкал</span>
              </div>
            </SwiperSlide>
            <SwiperSlide
              class="main__slider-slide"
              @click="$router.push('/tours/1/')"
            >
              <img src="@/assets/img/eda3.jpg" class="main__slider-slide-img" />
              <div class="main__slider-info">
                <span class="main__slider-slide-title"
                  >Дагестанский шашлык</span
                >
              </div>
            </SwiperSlide>
          </Swiper>
        </div>
        <div class="main__slider">
          <Swiper
            :modules="modules"
            class="main__slider-wrapper"
            :slides-per-view="3"
            :space-between="20"
          >
            <SwiperSlide
              class="main__slider-slide"
              @click="$router.push('/tours/1/')"
            >
              <img
                src="@/assets/img/slide1.jpg"
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
            <SwiperSlide
              class="main__slider-slide"
              @click="$router.push('/tours/1/')"
            >
              <img
                src="@/assets/img/slide2.jpg"
                class="main__slider-slide-img"
              />
              <div class="main__slider-info">
                <span class="main__slider-slide-title"
                  >Прогулка на катере по Сулакскому Каньону</span
                >
                <div class="main__slider-slider-subinfo">
                  <div class="main__slider-slider-time">12 часов</div>
                  <div class="main__slider-slider-peoples">12 чел</div>
                  <div class="main__slider-slider-cost">₽ 5 000</div>
                </div>
              </div>
            </SwiperSlide>
            <SwiperSlide
              class="main__slider-slide"
              @click="$router.push('/tours/1/')"
            >
              <img
                src="@/assets/img/slide3.jpg"
                class="main__slider-slide-img"
              />
              <div class="main__slider-info">
                <span class="main__slider-slide-title"
                  >Увидеть вживую Хунзахский водопат</span
                >
                <div class="main__slider-slider-subinfo">
                  <div class="main__slider-slider-time">12 часов</div>
                  <div class="main__slider-slider-peoples">12 чел</div>
                  <div class="main__slider-slider-cost">₽ 11 000</div>
                </div>
              </div>
            </SwiperSlide>
          </Swiper>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import { Swiper, SwiperSlide, useSwiper } from "swiper/vue";
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
        products: [
          // {
          //   id: 1,
          //   title: "Чуду",
          //   img: require("./assets/img/eda1.jpg"),
          // },
          // {
          //   id: 2,
          //   title: "Аварский хинкал",
          //   img: require("./assets/img/eda1.jpg"),
          // },
          // {
          //   id: 3,
          //   title: "Курзе",
          //   img: require("./assets/img/eda1.jpg"),
          // },
        ],
        link: "/foods/1",
      };
    },
  };
</script>

<style scoped>
  .tours {
    margin-top: 120px;
  }
  .container {
    max-width: 1240px;
    margin: 0 auto;
  }
  .tours__title {
    margin: 16px 0 8px;
    font-weight: 800;
    font-size: 38px;
    line-height: 45px;
  }
  .tours__subtitle {
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    color: #666666;
  }
  .tours__back {
    position: relative;
    padding-left: 30px;
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    color: #26b872;
    text-decoration: none;
  }
  .tours__back::before {
    content: "";
    position: absolute;
    left: 0;
    top: 1px;
    width: 20px;
    height: 20px;
    background-image: url("~/assets/img/icon/back.svg");
  }

  .tours__item {
    width: 100%;
    height: 293px;
    display: flex;
    flex-wrap: nowrap;
    overflow-x: scroll;
    padding-bottom: 20px;
    column-gap: 20px;
  }

  .tours__wrap {
    width: 1240px;
    display: flex;
    flex-direction: row;
    gap: 20px;
  }

  .product-card {
    max-width: 100%;
    max-height: 100%;
    width: 100%;
    height: 100%;
    border-radius: 12px;
    overflow: hidden;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
  }

  @media (max-width: 800px) {
    .tours {
      margin-top: 85px;
    }
    .tours__title {
      margin: 16px 0 12px;
      font-size: 32px;
      line-height: 38px;
    }
  }

  .main__slider {
    margin-bottom: 20px;
  }
  .tours__subtitle {
    margin-bottom: 40px;
  }
</style>

<style scoped>
  /* SLIDER */

  .main__slider-slide {
    position: relative;
    width: 100%;
    min-width: 350px;
    height: 294px;
    overflow: hidden;
    background-color: gray;
    border-radius: 12px;
    cursor: pointer;
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
