<script setup>
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import file2 from './components/file2.vue';

const showMotorList = ref(false);
const selectedMotor = ref('');

const handleMotorData = (motor) => {
  selectedMotor.value = motor;
};

</script>


<template>

<div class="container">
  <div class="box">
    <h1>Spesifikasi Motor Yamaha</h1>
    <p>Yamaha adalah produsen sepeda motor terkenal yang dikenal karena desainnya yang inovatif dan kinerja yang andal.</p>
    <button @click="showMotorList = !showMotorList">
      {{ showMotorList ? 'Sembunyikan' : 'Tampilkan' }} Daftar Motor
    </button>
    <HelloWorld v-if="showMotorList" @motorData="handleMotorData" />
    <div v-if="selectedMotor">
      <h2>Detail Motor:</h2>
      <p>{{ selectedMotor }}</p>
    </div>
    <file2 :selectedMotor="selectedMotor" />
  </div>
  </div>
</template>


