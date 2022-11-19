<template>
  <div class="tours">
    <NuxtLink to="/" class="tours__back">Назад на главную</NuxtLink>
    <div class="tours__title">Туры</div>
    <div class="tours__subtitle">Здесь отображены все туры</div>
    <div class="tours__wrap">
      <div class="tours__item">
        <Product
          v-for="(product, index) in products[0]"
          :key="product.id"
          :product="product"
          class="product-card"
        />
      </div>
    </div>
    <div class="tours__wrap">
      <div class="tours__item">
        <Product
          v-for="(product, index) in products[0]"
          :key="product.id"
          :product="product"
          class="product-card"
        />
      </div>
    </div>
    <div class="tours__wrap">
      <div class="tours__item">
        <Product
          v-for="(product, index) in products[0]"
          :key="product.id"
          :product="product"
          class="product-card"
        />
      </div>
    </div>
  </div>
</template>

<script>
  export default {
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
      };
    },
  };
</script>

<style scoped>
  .tours {
    margin-top: 120px;
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
    margin: 24px -60px 0;
  }

  .product-card:first-child {
    margin-left: 20px;
  }
  .product-card:last-child {
    margin-right: 20px;
  }
</style>
