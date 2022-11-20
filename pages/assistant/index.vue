<template>
  <div class="assistant">
    <div v-if="step === 0" class="assistant__1">
      <Babl v-for="(b, i) in babls" :key="i" :texts="b.text" />
    </div>
    <div v-if="step === 1" class="assistant__1">
      <Babl
        texts="Но сейчас мы познакомим вас с нашей культурой и с нашими местными достопримечательностями и местами!"
      />
      <img src="~/assets/img/as-2.jpg" class="assistant__img" />
    </div>
    <div v-if="step === 2" class="assistant__1">
      <Babl v-for="(b, i) in babls2" :key="i" :texts="b.text" />
      <Checkbox name="Больше 25 лет" key="a" />
      <Checkbox name="Больше 30 лет" key="b" />
      <Checkbox name="Меньше 40 лет" key="c" />
    </div>
    <div v-if="step === 3" class="assistant__1">
      <Babl texts="Что из этого вы больше предпочитаете?" />
      <Checkbox name="Горы" />
      <Checkbox name="Море" />
      <Checkbox name="Достопримечательности" />
    </div>
    <div v-if="step === 4" class="assistant__1">
      <Babl texts="Еще вопрос! Что из этого вы больше предпочитаете?" />
      <Checkbox name="Историю" />
      <Checkbox name="Эмоции, впечатления" />
    </div>
    <Button v-if="step === 0" @click="NextStep" class="btn"
      >Давайте дальше</Button
    >
    <Button v-if="step === 1" @click="NextStep" class="btn"
      >Как красиво!</Button
    >
    <Button v-if="step === 2" @click="NextStep" class="btn"
      >С этим разобрались, что дальше?</Button
    >
    <Button v-if="step === 3" @click="NextStep" class="btn">Вперед!</Button>
    <Button
      v-if="step === 4"
      @click="NextStep, $router.push('/tours/')"
      class="btn"
      >Завершить и подобрать!</Button
    >
  </div>
</template>

<script>
  export default {
    data() {
      return {
        babls: [
          {
            text: "Чем мы отличаемся от других субьектов РФ? Давайте расскажем правила нашей уникальной культуры подробнее!",
          },
          {
            text: "Не носить короткую одежду!",
          },
          {
            text: "Не оголяться",
          },
          {
            text: "Не мусорить",
          },
          {
            text: "Быть трезвым",
          },
          {
            text: "Не матерится в общественных местах",
          },
        ],
        babls2: [
          {
            text: "Не знаете что выбрать? Как определиться? Давайте я вам помогу!",
          },
          {
            text: "Сколько вам лет?",
          },
        ],
        step: 0,
      };
    },
    methods: {
      NextStep() {
        this.step += 1;
      },
    },
  };
</script>

<style scoped>
  .assistant {
    max-width: 400px;
    margin: 0 auto;
    margin-top: 90px;
  }
  .assistant__1 {
    display: flex;
    flex-direction: column;
    row-gap: 16px;
  }
  .assistant__img {
    max-width: 400px;
  }

  .btn {
    margin-top: 24px;
  }
</style>
