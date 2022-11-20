<template>
  <div class="babl">
    {{ texts }}
  </div>
</template>

<script>
  export default {
    props: {
      texts: {
        type: String,
      },
    },
  };
</script>

<style scoped>
  .babl {
    padding: 16px;
    background: #f5f5f5;
    border-radius: 24px 32px 24px 0px;
  }
</style>
