<template>
  <div class="tour">
    <div class="tour__top">
      <img src="~/assets/img/tour1.jpg" alt="Гамсутль" class="tour__top-img" />
      <div class="container">
        <NuxtLink to="/" class="tour__link">
          <div class="tours__back">Назад на главную</div>
        </NuxtLink>
      </div>
    </div>
    <div class="container">
      <div class="tour__info">
        <div class="tour__info-top">
          <div class="tour__info-icon-wrap">
            <img src="~/assets/img/tour-e.jpg" class="tour__info-icon" alt="" />
          </div>
          <div class="tour__info-btns">
            <Button>Оставить заявку</Button>
            <Button theme="blue">Оставить отзыв</Button>
          </div>
        </div>
        <div class="tour__info-title">
          Экскурсия в Гамсутль, купи да по братски
        </div>
      </div>
      <div class="tour__info-items">
        <div class="tour__info-time">12 часов</div>
        <div class="tour__info-count">12 человек</div>
        <div class="tour__info-price">₽ 20 000</div>
      </div>
      <div class="tour__info-desc">Описание</div>
      <div class="tour__info-subtitle">
        Магма обогащает лимнический конус выноса, где присутствуют моренные
        суглинки днепровского возраста. В противоположность этому руководящее
        ископаемое существенно разогревает протерозой, так как совершенно
        однозначно указывает на существование и рост в период оформления
        палеогеновой поверхности выравнивания.
      </div>
      <div class="tour__info-slider">
        <div class="tour__info-slide">
          <img
            class="tour__info-slide-img"
            src="~/assets/img/tour-1-slide.jpg"
            alt=""
          />
        </div>
        <div class="tour__info-slide">
          <img
            class="tour__info-slide-img"
            src="~/assets/img/tour-2-slide.jpg"
            alt=""
          />
        </div>
        <div class="tour__info-slide">
          <img
            class="tour__info-slide-img"
            src="~/assets/img/tour-3-slide.jpg"
            alt=""
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {};
</script>

<style scoped>
  .container {
    max-width: 1280px;
    padding: 0px 20px;
    margin: 0 auto;
  }
  .tours__back {
    position: relative;
    padding-left: 30px;
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;

    color: #000000;
    text-decoration: none;
  }
  .tours__back::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 24px;
    height: 24px;
    background-image: url("~/assets/img/icon/arrow-left-m.svg");
  }

  .tour__link {
    position: absolute;
    top: 24px;
    display: block;
    text-decoration: none;
    padding: 14px 16px;
    background: #ffffff;
    border-radius: 43px;
  }

  .tour__top {
    position: relative;
    min-height: 250px;
    margin: 71px -20px 0;
  }
  .tour__top-img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .tour__info {
    margin-top: 24px;
  }

  .tour__info-icon-wrap {
    max-width: 100px;
  }
  .tour__info-icon {
    width: 100%;
  }

  .tour__info-title {
    margin: 5px 0px 12px;
    font-weight: 700;
    font-size: 32px;
    line-height: 38px;
  }

  .tour__info-items {
    display: flex;
    column-gap: 20px;
  }
  .tour__info-time {
    position: relative;
    padding-left: 30px;
    font-size: 18px;
    line-height: 21px;
  }
  .tour__info-time::before {
    content: "";
    position: absolute;
    left: 0;
    top: -2px;
    width: 24px;
    height: 24px;
    background-image: url(~/assets/img/icon/clock.svg);
    font-size: 18px;
    line-height: 21px;
  }
  .tour__info-count {
    position: relative;
    padding-left: 30px;
    font-size: 18px;
    line-height: 21px;
  }
  .tour__info-count::before {
    content: "";
    position: absolute;
    left: 0;
    top: -2px;
    width: 24px;
    height: 24px;
    background-image: url(~/assets/img/icon/user.svg);
    font-size: 18px;
    line-height: 21px;
  }
  .tour__info-price {
    font-size: 18px;
    line-height: 21px;
  }

  .tour__info-desc {
    margin-top: 32px;
    font-weight: 700;
    font-size: 25px;
    line-height: 30px;
  }

  .tour__info-subtitle {
    margin-top: 12px;
    font-size: 18px;
    line-height: 25px;
  }

  .tour__info-slide {
    min-width: 400px;
  }
  .tour__info-slide:first-child {
    margin-left: 20px;
  }
  .tour__info-slide:last-child {
    margin-right: 20px;
  }
  .tour__info-slide-img {
    width: 100%;
  }

  .tour__info-slider {
    display: flex;
    column-gap: 20px;
    margin: 0px -20px;
    flex-wrap: nowrap;
    overflow-x: scroll;
  }

  .tour__info-slider::-webkit-scrollbar {
    display: none;
  }

  .tour__info-top {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
  }

  .tour__info-btns {
    display: flex;
    column-gap: 16px;
  }
</style>
