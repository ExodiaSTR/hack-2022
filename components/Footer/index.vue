<template>
  <div class="footer">
    <div class="footer__items">
      <div class="footer__item">Все права не защищены</div>
      <div class="footer__item">
        <img
          src="~/assets/img/footer.png"
          class="footer__item-img"
          alt="Powered by students from"
        />
      </div>
    </div>
  </div>
</template>

<script></script>

<style scoped>
  .footer {
    margin: 100px -20px 0;
    background-color: #212121;
    padding: 25px 0px;
    color: #fff;
  }

  .footer__items {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1280px;
    margin: 0 auto;
    padding: 0px 20px;
  }

  .footer__item {
    max-width: 325px;
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
  }
  .footer__item-img {
    width: 100%;
  }
</style>
