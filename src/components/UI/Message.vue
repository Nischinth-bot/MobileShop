<template>
  <div class="container">
    <h1><slot> </slot></h1>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
h1 {
  background: white;
  padding: 20px 20px;
  color: orange;
  animation: right-to-left 15s infinite ease-in-out;
  position: relative;
}

@keyframes right-to-left {
  0% {
    left: 100%;
  }
  100% {
    left: -100%;
  }
}
</style>