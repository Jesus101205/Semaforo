<template>
  <div class="rojo" :class="{ 'onrojo': isOn }"></div>
</template>

<script>
export default {
  props: ['isOn']
}
</script>

<style>
.rojo {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  margin-top: -20px;
  background-color: red;
}

.onrojo {
  background-color: rgba(255, 0, 0, 0.1);
}
</style>