<template>
    <div v-if="selectedMotor" class="container2">
      <h3>Spesifikasi Motor: {{ selectedMotor }}</h3>
      <p>{{ getMotorSpecification(selectedMotor) }}</p>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue';
  
  const props = defineProps({
    selectedMotor: {
      type: String,
      required: true
    }
  });
  
  const getMotorSpecification = (motor) => {
    // Return the specification based on the selected motor
    switch (motor) {
      case 'Yamaha R15':
        return '155cc, 19.3 PS, 14.7 Nm';
      case 'Yamaha Vixion':
        return '150cc, 16.36 PS, 14.5 Nm';
      case 'Yamaha NMAX':
        return '155cc, 15.1 PS, 13.9 Nm';
      case 'Yamaha MT-15':
        return '155cc, 19.3 PS, 14.7 Nm';
      default:
        return '';
    }
  };
  </script>
  