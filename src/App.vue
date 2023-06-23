<script>
import Header from './components/common/Header.vue'

export default {
  components: {
    Header
  }
}
</script>

<template>
  <Header />
  <div className="content">
    <router-view />
  </div>
</template>

<style scoped>
.content {
  margin: 20px auto;
  width: 90%;
  max-width: 1000px;
  min-height: 70vh;
  background-color: #fff;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}
</style>
