<template>
  <button :class="['button', `button_${theme}`, { fluid: fluid }]">
    <slot>Текст на кнопке</slot>
  </button>
</template>

<script>
  export default {
    props: {
      fluid: {
        type: Boolean,
        default: false,
      },
      theme: {
        type: String,
        default: "green",
      },
    },
  };
</script>

<style scoped>
  .button {
    padding: 12px 24px;
    font-size: 18px;
    line-height: 21px;
    border-radius: 12px;
    color: #fff;
    background-color: transparent;
    cursor: pointer;
    outline: none;
    border: 0;
    transition: all 0.5s;
  }
  .fluid {
    width: 100%;
  }

  .button_green {
    background-color: #26b872;
  }
  .button_green:hover {
    background-color: #379a6b;
  }
  .button_blue {
    background-color: #267ab8;
  }
  .button_blue:hover {
    background-color: #2771a7;
  }
  .button_border-green {
    color: #26b872;
    border: 1px solid #26b872;
  }
  .button_border-green:hover {
    background-color: #379a6b;
    color: #fff;
  }
  .button_border-blue {
    color: #267ab8;
    border: 1px solid #267ab8;
  }
  .button_border-blue:hover {
    background-color: #267ab8;
    color: #fff;
  }
  .button_border-outline-g {
    color: #26b872;
    padding: 0;
    border: transparent;
  }
  .button_border-outline-b {
    padding: 0;
    color: #267ab8;
    border: transparent;
  }
</style>
