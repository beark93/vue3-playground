<script>
import Timer from '../components/game/Timer.vue'

export default {
  data() {
    return {
      time: 13,
      timer: null
    }
  },
  components: {
    Timer
  },
  methods: {
    onClickStart() {
      if (!this.timer) {
        this.timer = setInterval(() => {
          if (this.time >= 0.02) {
            this.time -= 0.02
          } else {
            this.time = 0
            clearInterval(this.timer)
          }
        }, 20)
      }
    }
  },
  beforeUnmounted() {
    if (this.timer) {
      clearInterval(this.timer)
    }
  }
}
</script>

<template>
  <Timer :time="time" />
  <div className="game-zone">
    <button className="game-zone__start-btn" @click.prevent="onClickStart">Start</button>
  </div>
</template>

<style scoped>
.game-zone {
  position: relative;
  width: 100%;
  padding: 10px;
  text-align: center;
}

.game-zone .game-zone__start-btn {
  padding: 10px 15px;
  font-size: 20px;
  border: 0px;
  border-radius: 10px;
  color: white;
  background-color: limegreen;
  cursor: pointer;
}
</style>