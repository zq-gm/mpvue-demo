<template>
  <div>
    <p class="card">
      {{text}}
    </p>
    <div>
      <input value="第一个demo">
    </div>
  </div>
</template>

<script>
export default {
  props: ['text']
}
</script>

<style>
.card {
  padding: 10px;
}
</style>
