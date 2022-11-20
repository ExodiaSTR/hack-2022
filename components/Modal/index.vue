<template>
  <div class="modal" @click="$emit('close')">
    <div class="modal-window">
      <div
        @click.stop.prevent
        class="modal-close"
        @click="$emit('close')"
      ></div>
    </div>
  </div>
</template>

<script>
  export default {};
</script>

<style scoped>
  .modal {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);

    display: flex;
    justify-content: center;
    align-items: center;
  }
  .modal-window {
    position: relative;
    width: 500px;
    padding: 20px;

    border-radius: 12px;
    background-color: white;
    overflow: hidden;
  }
  .modal-close {
    position: absolute;
    transform: translateY(-50%);
    right: 20px;
    width: 20px;
    height: 20px;
    background-image: url(@/assets/img/icon/x.svg);
    background-repeat: no-repeat;
    background-position: center;
  }
</style>
