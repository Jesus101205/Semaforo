<template>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" />

  <div class="traffic-light-container">
    <div class="traffic-light">
      <rojo :isOn="isRedLightOn" />
      <amarillo :isOn="isYellowLightOn" />
      <verde :isOn="isGreenLightOn" />
    </div>

    <div class="button-container">
    </div>

    <button type="button" class="btn btn-info btn-sm mb-3" @click="Cambiar">PARE</button>
    <button type="button" class="btn btn-info btn-sm mb-3" @click="Cambiar2">ATENTO</button>
    <button type="button" class="btn btn-info btn-sm mb-3" @click="Cambiar3">SIGA</button>
  
  </div>
</template>

<script>
export default {
  data() {
    return {
      isRedLightOn: true,
      isYellowLightOn: true,
      isGreenLightOn: true,
    };
  },
  methods: {
    Cambiar() {
      this.isRedLightOn = false;
      this.isYellowLightOn = true;
      this.isGreenLightOn = true;
    },
    Cambiar2() {
      this.isYellowLightOn = false;
      this.isRedLightOn = true;
      this.isGreenLightOn = true;
    },
    Cambiar3() {
      this.isGreenLightOn = false;
      this.isRedLightOn = true;
      this.isYellowLightOn = true;
    },
  },
};
</script>

<style scoped>
.traffic-light-container {
  background-image: url('/public/fondo.jpg');
  height: 100vh;
  display: flex;
  flex-direction: column;
}

.traffic-light {
  width: 435px;
  height: 557px;
  border-radius: 25px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  padding: 20px;
  position: relative;
  background-image: url('/public/semaforo.png');
}

.button-container {
  margin-top: -30px;
  background-color: rgb(87, 86, 86);
  padding: 15px;
  height: 300px;
  width: 45px;
  margin-left: 200px;
}
</style>