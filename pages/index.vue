<template>
    <div>
      <h1>Bem-vindo à Página de Confetti!</h1>
      <ConfettiButton />
    </div>
  </template>
  
  <script setup>
  // Importando o componente ConfettiButton
  import ConfettiButton from '~/components/ConfettiButton.vue'
  </script>
  
  <style scoped>
  h1 {
    text-align: center;
    margin-top: 40px;
    font-size: 28px;
  }
  </style>
  