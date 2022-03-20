<template>
  <div>
    <div class="counter-num">次数：{{num}}</div>
    <span>
      <button class="counter-btn" @click="handleClick">点我呀！</button>
      <button class="counter-reset-btn" @click="handleResetClick">清零</button>
    </span>
  </div>
</template>

<script>
  export default {
    name: 'jiShu',
    data () {
      return {
        num: 0
      }
    },
    methods: {
      handleClick () {
        this.num = this.num + 1
      },
      handleResetClick () {
        this.num = 0
      }
    }
  }
</script>

<style scoped>
  .click-counter {
    display: flex;
    align-items: center;
    justify-content: center;
    border: 1px solid red;
    background-color: #ffffff;
    padding: 10px;
  }

  .counter-num,
  .counter-btn,
  .counter-reset-btn {
    flex: 1;
    margin: 3px;
  }
</style>
