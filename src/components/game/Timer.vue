<script>
export default {
  props: ['time']
}
</script>

<template>
  <div className="timer">
    {{ time.toFixed(2) }}
  </div>
</template>

<style scoped>
.timer {
  position: relative;
  width: 100%;
  padding: 10px;
  font-size: 50px;
  text-align: center;
}
</style>