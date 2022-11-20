<template>
  <div class="tours">
    <div class="container">
      <NuxtLink to="/" class="tours__back">Назад на главную</NuxtLink>
      <div class="tours__title">Туры</div>
      <div class="tours__subtitle">Здесь отображены все туры</div>
      <div class="tours-content">
        <div class="tours__wrap">
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
              <SwiperSlide
                class="main__slider-slide"
                @click="$router.push('/tours/1/')"
              >
                <img
                  src="@/assets/img/slide4.jpg"
                  class="main__slider-slide-img"
                />
                <div class="main__slider-info">
                  <span class="main__slider-slide-title">Бархан Сарыкум></span>
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
        <div class="tours__wrap">
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
              <SwiperSlide
                class="main__slider-slide"
                @click="$router.push('/tours/1/')"
              >
                <img
                  src="@/assets/img/slide4.jpg"
                  class="main__slider-slide-img"
                />
                <div class="main__slider-info">
                  <span class="main__slider-slide-title">Бархан Сарыкум></span>
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
        <div class="tours__wrap">
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
              <SwiperSlide
                class="main__slider-slide"
                @click="$router.push('/tours/1/')"
              >
                <img
                  src="@/assets/img/slide4.jpg"
                  class="main__slider-slide-img"
                />
                <div class="main__slider-info">
                  <span class="main__slider-slide-title">Бархан Сарыкум></span>
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
          [
            {
              id: 1,
              img: "~/assets/img/slide1.jpg",
              title: "Путешествие к Эльбрусу и озеру Гижгит",
              time: "12 часов",
              count: "12 чел",
              price: "20 000",
            },
            {
              id: 2,
              imgKey: "slide2",
              title: "Путешествие к Эльбрусу и озеру Гижгит",
              time: "12 часов",
              count: "12 чел",
              price: "20 000",
            },
            {
              id: 3,
              imgKey: "slide3",
              title: "Путешествие к Эльбрусу и озеру Гижгит",
              time: "9 часов",
              count: "5 чел",
              price: "15 000",
            },
          ],
        ],
        link: "/tours/1",
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

  .tours-content {
    margin-bottom: 30px;
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
    display: flex;
    flex-wrap: nowrap;
    overflow-x: scroll;
    margin: 0 -40px -20px;
    padding-bottom: 20px;
    column-gap: 20px;
  }
  .tours__item::-webkit-scrollbar {
    display: none;
  }
  .tours__item:last-child {
    margin-right: 40px;
  }
  .tours__item:first-child {
    margin-left: 40px;
  }

  .tours__wrap {
    display: flex;
    flex-direction: column;
    margin-bottom: 30px;
  }

  .product-card:first-child {
    margin-left: 20px;
  }
  .product-card:last-child {
    margin-right: 20px;
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
    .slider__link {
      display: none;
    }
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
