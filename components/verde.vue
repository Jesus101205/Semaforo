<template>
  <div class="verde" :class="{ 'onverde': isOn }"></div>
</template>

<script>
export default {
  props: ['isOn']
}
</script>

<style>
.verde {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  margin-top: -200px;
  background-color: lime;
}

.onverde {
  background-color: rgba(0, 255, 0, 0.1);
}
</style>