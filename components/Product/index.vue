<template>
  <div class="product">
    <img class="product__img" src="~/assets/img/slide1.jpg" alt="" />
    <div class="main__slider-info">
      <span class="main__slider-slide-title">{{ product.title }}</span>
      <div class="main__slider-slider-subinfo">
        <div class="main__slider-slider-time">{{ product.time }}</div>
        <div class="main__slider-slider-peoples">{{ product.count }}</div>
        <div class="main__slider-slider-cost">₽ {{ product.price }}</div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      product: {
        type: Object,
        default: () => {},
      },
    },
  };
</script>

<style scoped>
  .product {
    position: relative;
    min-width: 400px;
    height: 294px;

    overflow: hidden;
    background-color: gray;
    border-radius: 12px;
  }

  .product__img {
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
