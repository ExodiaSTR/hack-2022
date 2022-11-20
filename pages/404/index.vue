<template>
  <div class="error">
    <div class="error__img-wrap">
      <img src="~/assets/img/error-fon.jpg" class="error__img-fon" alt="404" />
      <img src="~/assets/img/error.jpg" class="error__img" alt="" />
    </div>
  </div>
</template>

<script></script>

<style scoped>
  .error__img-wrap {
    position: relative;
  }
  .error__img-fon {
    width: 100%;
  }

  .error__img {
    max-width: 320px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%);
  }
</style>
