<template>
  <div class="food">
    <div class="container">
      <NuxtLink :to="link" class="tours__back">Назад на главную</NuxtLink>
      <div class="tours__title">Национальные блюда</div>
      <div class="tours__subtitle">
        Мы вам покажем национальные блюда Дагестана!
      </div>
      <div class="food__wrapper">
        <div class="food-img-wrap">
          <img src="~/assets/img/food-main.jpg" alt="" class="food-img" />
        </div>
        <div class="food__left">
          <img src="~/assets/img/hash-food.jpg" class="food__left-img" alt="" />
          <div class="food__left-title">Чуду</div>
          <div class="food__left-descr">
            блюдо народов Дагестана, входит в даргинскую, кумыкскую и другие
            национальные кухни. Представляет собой тонкие, либо толстые пресные
            лепёшки с начинкой, обжаренные на сухой сковороде. По форме чуду
            бывают как круглые, так и полукруглые.
          </div>
          <div class="food__left-subtitle">Где это можно поесть?</div>
          <div class="food__left-position">Hinkal Brother, Махачкала</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {};
</script>

<style scoped>
  .food {
    margin-top: 95px;
  }
  .container {
    max-width: 1240px;
    margin: 0 auto;
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
  .food-img-wrap {
    max-width: 540px;
  }
  .food__wrapper {
    margin-top: 20px;
    display: flex;
    column-gap: 20px;
  }
  .food-img {
    width: 100%;
  }
  .food__left-img {
    max-width: 214px;
    margin-bottom: 12px;
  }

  .food__left-title {
    margin-bottom: 20px;
    font-weight: 700;
    font-size: 38px;
    line-height: 45px;
  }
  .food__left-subtitle {
    margin-bottom: 8px;
    font-weight: 700;
    font-size: 25px;
    line-height: 140%;
  }

  .food__left-descr {
    font-weight: 500;
    font-size: 18px;
    line-height: 140%;
    margin-bottom: 32px;
  }

  .food__left-position {
    font-weight: 500;
    font-size: 18px;
    line-height: 140%;
    color: #267ab8;
    cursor: pointer;
  }

  @media (max-width: 800px) {
    .tours__back {
      padding-left: 30px;
      font-weight: 500;
      font-size: 18px;
      line-height: 21px;
    }
    .tours__title {
      font-weight: 800;
      margin: 16px 0px 8px;
      font-size: 25px;
      line-height: 30px;
    }

    .tours__subtitle {
      font-size: 16px;
    }
    .food__wrapper {
      flex-direction: column;
    }

    .food-img-wrap {
      max-width: none;
      max-height: 250px;
      margin-bottom: 20px;
      margin: 0px -20px;
    }
    .food-img {
      max-height: 250px;
      object-fit: cover;
      border-radius: 12px;
    }

    .food__left-img {
      margin-bottom: 8px;
    }

    .food__left-title {
      font-size: 38px;
      line-height: 45px;
      margin-bottom: 16px;
    }

    .food__left-descr {
      font-size: 18px;
      line-height: 140%;
      color: #666666;
      margin-bottom: 24px;
    }
  }
</style>
