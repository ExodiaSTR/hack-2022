<template>
  <div class="layout">
    <Header />
    <div class="layout__content">
      <slot />
    </div>
    <Footer />
    <Modal
      v-if="showModal"
      @close="showModal = false"
      @open="showModal = true"
    />
  </div>
</template>

<script>
  export default {
    data() {
      return {
        showModal: false,
      };
    },
  };
</script>

<style>
  .layout {
    padding: 0px 20px;
    overflow-x: hidden;
  }
  /* .layout__content {
    max-width: 1280px;
    margin: 80px auto 0;
  } */
</style>
