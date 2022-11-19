<template>
  <div class="layout">
    <Header />
    <div class="layout__content">
      <slot />
    </div>
  </div>
</template>

<style>
  .layout {
    padding: 0px 20px;
    overflow-x: hidden;
  }
  .layout__content {
    max-width: 1280px;
    padding: 0px 20px;
    margin: 80px auto 0;
  }
</style>
