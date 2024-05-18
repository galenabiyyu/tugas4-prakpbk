<template>
  <div class="container1">
    <h2>Daftar Motor Yamaha</h2>
    <ul>
      <li v-for="motor in motors" :key="motor">
        {{ motor }}
        <button @click="selectMotor(motor)">Lihat Spesifikasi</button>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { defineEmits } from 'vue';

const emits = defineEmits(['motorData']);

const motors = ['Yamaha R15', 'Yamaha Vixion', 'Yamaha NMAX', 'Yamaha MT-15'];

const selectMotor = (motor) => {
  emits('motorData', motor);
};
</script>



