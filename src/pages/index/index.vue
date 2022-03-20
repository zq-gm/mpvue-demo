<template>
  <div>
    <span class="center" @click="clickme">点我</span>
    <div class="message">{{message}}</div>
    <div>计数：{{time}}</div>
    <button @click="getTime">开始</button>
    <button @click="clearTime">清零</button>
    <ji-shu/>
    <ji-shu/>
    <ji-shu/>
  </div>
</template>

<script>
import jiShu from '@/components/jiShu/jiShu'
export default {
  name: 'index',
  components: { jiShu },
  data () {
    return {
      message: 'hello',
      and: 0,
      time: 0,
      able: true,
      timeFlag: false
    }
  },
  methods: {
    getTime () {
      this.able = false
      this.timeFlag = setInterval(this.setTime, 1000)
    },
    setTime () {
      this.time += 1
    },
    clearTime () {
      if (this.timeFlag) {
        this.time = 0
        clearInterval(this.timeFlag)
      }
    },
    clickme () {
      if (this.message === '程序员') {
        this.message = '加油'
      } else {
        this.message = '程序员'
      }
    },
    add () {
      this.and = 5 + 3
    }
  }
}
</script>

<style scoped>
  .message {
    color: red;
    padding: 10px;
    text-align: center;
  }
</style>
