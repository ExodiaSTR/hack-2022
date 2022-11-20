<template>
  <div class="checkbox">
    <input
      id="check"
      type="checkbox"
      :value="value"
      class="checkbox__input"
      :checked="checked"
      @change="onChange"
    />
    <label for="check" class="checkbox__text">
      <slot>{{ name }}</slot>
    </label>
  </div>
</template>

<script>
  export default {
    model: {
      prop: "checked",
      event: "change",
    },
    props: {
      name: {
        type: String,
        default: "",
      },
      value: [String, Number],
      checked: {
        type: Boolean,
        default: false,
      },
    },
    methods: {
      onChange(event) {
        this.$emit("change", event.target.checked, this.value);
      },
    },
  };
</script>

<style scoped>
  .checkbox {
    position: relative;
    display: flex;
    align-items: center;
    column-gap: 10px;
    padding: 12px 16px;
    border: 1px solid #26b872;
    border-radius: 12px;
  }
  .checkbox__text {
    padding-left: 30px;
    font-size: 18px;
    line-height: 21px;
    color: #000;
  }
  .checkbox__input {
    width: 20px;
    height: 20px;
    padding: 5px 3px;
    position: relative;
    display: inline-block;
    border: 1px solid #e5e5e5;
    background-color: #fff;
    border-radius: 6px;
    cursor: pointer;
    vertical-align: top;
    outline: none;
    flex-shrink: 0;
    display: none;
  }
  .checkbox__input ~ label::before {
    content: "";
    position: absolute;
    width: 20px;
    height: 20px;
    left: 16px;
    border: 1px solid #e5e5e5;
    border-radius: 4px;
  }

  .checkbox__input:checked ~ label::before {
    content: "";
    background-image: url("~/assets/img/icon/check.svg");
    background-repeat: no-repeat;
    background-position: 50% 50%;
    background-size: 15px;
  }
</style>
