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
        <NuxtLink class="header__link" to="/">Туры / Экскурсии</NuxtLink>
        <NuxtLink class="header__link" to="/">Отель</NuxtLink>
        <NuxtLink class="header__link" to="/">Еда</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
  export default {};
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
</style>
