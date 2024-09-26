<template>
    <div class="confetti-container">
      <button @click="triggerConfetti">Lançar Confete 🎉</button>
    </div>
  </template>
  
  <script setup>
  // Importando a biblioteca de confete
  import confetti from 'canvas-confetti'
  
  const triggerConfetti = () => {
    const end = Date.now() + 15 * 1000;

      // go Buckeyes!
    const colors = ["#0000CD", "#B8860B"];

      (function frame() {
        confetti({
          particleCount: 2,
          angle: 60,
          spread: 55,
          origin: { x: 0 },
          colors: colors,
        });

        confetti({
          particleCount: 2,
          angle: 120,
          spread: 55,
          origin: { x: 1 },
          colors: colors,
        });

        if (Date.now() < end) {
          requestAnimationFrame(frame);
        }
    })();
  };
  </script>
  
  <style scoped>
  .confetti-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
  }
  
  button {
    padding: 10px 20px;
    font-size: 18px;
    background-color: #ff4081;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  button:hover {
    background-color: #ff1e70;
  }
  </style>
  