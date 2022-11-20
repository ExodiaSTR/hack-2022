<template>
  <div class="main">
    <section class="main__dagestan">
      <img
        src="~/assets/img/dagestan.jpg"
        alt="Дагестан"
        class="main__dagestan-img"
      />
      <img
        src="~/assets/img/dag05pudge.jpg"
        alt="Дагестан"
        class="main__dagestan-img-mobile"
      />
    </section>
    <NuxtLink to="/assistant/" class="main__help">
      <img
        src="~/assets/img/help.jpg"
        alt="Поможем определиться  с выбором"
        class="main__dagestan-img"
      />
      <img
        src="~/assets/img/help2.jpg"
        alt="Поможем определиться  с выбором"
        class="main__dagestan-img-mobile"
      />
    </NuxtLink>
    <section class="main__top">
      <div class="main__top-title">Возможно вам понравится</div>
      <div class="main__top-items">
        <NuxtLink to="/" class="top__item">
          <img
            src="~/assets/img/food-banner.jpg"
            alt="Национальная еда Дагестана"
            class="top__item-img"
          />
        </NuxtLink>
        <NuxtLink to="/" class="top__item">
          <img
            src="~/assets/img/factoid.jpg"
            alt="Национальная еда Дагестана"
            class="top__item-img"
          />
        </NuxtLink>
      </div>
    </section>
    <section class="main__slider-wrap">
      <div class="slider__top">
        <div class="slider__left">
          <p class="slider__title">Кажется нашли кое что для вас...</p>
          <p class="slider__subtitle">
            Построили экскурсии и туры на основе ваших интересов
          </p>
        </div>
        <NuxtLink to="/tours/" class="slider__link">Смотреть все туры</NuxtLink>
      </div>
      <Slider :slider="sliders" />
    </section>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        sliders: [
          {
            id: 1,
            img: "slide1",
            title: "Путешествие к Эльбрусу и озеру Гижгит",
            time: "12 часов",
            count: "12 чел",
            price: "20 000",
          },
          {
            id: 2,
            img: "slide2",
            title: "Путешествие к Эльбрусу и озеру Гижгит",
            time: "12 часов",
            count: "12 чел",
            price: "20 000",
          },
          {
            id: 3,
            img: "slide3",
            title: "Путешествие к Эльбрусу и озеру Гижгит",
            time: "9 часов",
            count: "5 чел",
            price: "15 000",
          },
          {
            id: 4,
            img: "slide3",
            title: "Путешествие к Эльбрусу и озеру Гижгит",
            time: "9 часов",
            count: "5 чел",
            price: "15 000",
          },
          {
            id: 5,
            img: "slide3",
            title: "Путешествие к Эльбрусу и озеру Гижгит",
            time: "9 часов",
            count: "5 чел",
            price: "15 000",
          },
        ],
      };
    },
  };
</script>
<style scoped>
  .top__item {
    display: block;
    max-width: 680px;
  }
  .main {
    margin-top: 100px;
  }
  .main__top-title {
    margin-bottom: 16px;
    font-weight: 800;
    font-size: 38px;
    line-height: 45px;
  }
  .main__top-items {
    width: 100%;
    display: flex;
    column-gap: 20px;
  }
  .top__item-img {
    width: 100%;
    height: 100%;
  }

  .main__dagestan-img {
    width: 100%;
  }
  .main__dagestan {
    margin-bottom: 24px;
  }

  .main__help {
    display: block;
    margin-bottom: 60px;
  }
  .main__slider-wrap {
    margin-top: 60px;
    width: 100%;

    overflow: hidden;
    background-color: transparent;
  }
  .container {
    max-width: 1280px;
    padding: 0px 20px;
    margin: 0 auto;
  }

  .slider__top {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .slider__title {
    margin-bottom: 8px;
    font-weight: 800;
    font-size: 38px;
    line-height: 45px;
  }
  .slider__subtitle {
    margin-bottom: 24px;
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    color: #666666;
  }
  .slider__link {
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    color: #26b872;
    cursor: pointer;
    text-decoration: none;
  }

  .main__dagestan-img-mobile {
    display: none;
  }
  @media screen and (max-width: 800px) {
    .main__dagestan-img {
      display: none;
    }
    .main__dagestan-img-mobile {
      display: block;
      max-width: 100%;
      max-height: 100%;
      width: 100%;
      height: 100%;
    }
    .main__dagestan-img {
      display: none;
    }
    .main__dagestan-img-mobile {
      display: block;
      max-width: 100%;
      max-height: 100%;
      width: 100%;
      height: 100%;
    }
    .main__top-items {
      flex-direction: column;
    }
    .top__item {
      margin-bottom: 6px;
    }
  }
</style>
