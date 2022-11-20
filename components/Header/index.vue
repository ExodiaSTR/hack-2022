<template>
  <div class="header">
    <div class="header__container">
      <NuxtLink to="/" class="header__logo">
        <img
          src="~/assets/img/logo.png"
          alt="Логотип"
          class="header__logo-img"
        />
      </NuxtLink>
      <div class="header__links">
        <NuxtLink class="header__link" to="/tours">Туры / Экскурсии</NuxtLink>
        <NuxtLink class="header__link" to="/">Отель</NuxtLink>
        <NuxtLink class="header__link" to="/foods/">Еда</NuxtLink>
      </div>

      <div @click="showModal = !showModal" class="header__burger"></div>
    </div>
    <div class="header__modal" v-if="showModal">
      <div @click="showModal = !showModal" class="header__modal-close"></div>

      <div class="header__modal-content">
        <NuxtLink
          @click="showModal = !showModal"
          class="header__link"
          to="/tours"
          >Туры / Экскурсии</NuxtLink
        >
        <NuxtLink @click="showModal = !showModal" class="header__link" to="/"
          >Отель</NuxtLink
        >
        <NuxtLink @click="showModal = !showModal" class="header__link" to="/"
          >Еда</NuxtLink
        >
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        showModal: false,
      };
    },
    computed: {},
  };
</script>

<style>
  .header {
    position: fixed;
    left: 0;
    width: 100%;
    padding: 18px 0px;
    background: rgba(255, 255, 255, 0.3);
    border-bottom: 1px solid #e5e5e5;
    backdrop-filter: blur(25px);
    z-index: 2;
  }
  .header__container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1280px;
    margin: 0 auto;
    padding: 0px 20px;
  }
  .header__logo {
    max-width: 113px;
  }
  .header__logo-img {
    width: 100%;
  }
  .header__links {
    display: flex;
    align-items: center;
    column-gap: 32px;
  }
  .header__link {
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    text-decoration: none;
    color: #000;
    transition: all 0.5s;
  }
  .header__link:hover {
    color: #26b872;
  }
  .header__burger {
    display: none;
  }

  @media screen and (max-width: 600px) {
    .header__links {
      display: none;
    }

    .header__burger {
      display: block;
      width: 25px;
      height: 25px;
      background-image: url(@/assets/img/icon/burger-menu.svg);
      background-repeat: no-repeat;
      background-position: center;
      background-size: cover;
    }
    .header__modal {
      position: fixed;
      top: 0;
      right: 0;
      height: 100vh;
      width: 80%;
      background-color: white;
      border-left: 1px solid gray;
    }
    .header__modal-content {
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      margin: 75px 30px;
    }
    .header__modal-close {
      position: absolute;
      top: 20px;
      right: 25px;
      width: 25px;
      height: 25px;
      background-image: url(@/assets/img/icon/x.svg);
      background-repeat: no-repeat;
      background-position: center;
    }
    .header__link {
      width: 100%;
      text-align: right;
      margin-bottom: 20px;
    }
  }
</style>
