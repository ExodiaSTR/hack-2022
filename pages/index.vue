<template>
  <div class="main">
    <section class="main__dagestan">
      <img
        src="~/assets/img/dagestan.jpg"
        alt="Дагестан"
        class="main__dagestan-img"
      />
    </section>
    <NuxtLink class="main__help">
      <img
        src="~/assets/img/help.jpg"
        alt="Поможем определиться  с выбором"
        class="main__dagestan-img"
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
  </div>
</template>

<style scoped>
  .top__item {
    display: block;
    max-width: 680px;
  }
  .main__top-title {
    margin-bottom: 16px;
    font-weight: 800;
    font-size: 38px;
    line-height: 45px;
  }
  .main__top-items {
    display: flex;
    column-gap: 20px;
  }
  .top__item-img {
    width: 100%;
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
</style>
