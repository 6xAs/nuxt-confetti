<template>
  <div class="min-h-screen flex flex-col bg-gray-50 font-poppins">
    <!-- Cabeçalho -->
    <header class="text-center py-6">
      <h1 class="text-4xl font-bold text-gray-800">TÍTULO PRINCIPAL</h1>
    </header>

    <!-- Conteúdo Centralizado -->
    <main class="flex-grow flex flex-col items-center justify-center">
      <!-- Círculo para Imagem -->
      <div class="w-48 h-48 bg-gray-300 rounded-full flex items-center justify-center mb-4">
        <!-- Placeholder da imagem -->
        <p class="text-gray-500">Imagem</p>
      </div>

      <!-- Nome da Pessoa -->
      <h2 class="text-xl font-semibold text-gray-700 mb-2">TEXTO 01</h2>
      <p class="text-lg font-bold text-gray-800 mb-4">NOME PESSOA</p>

      <!-- Texto adicional -->
      <p class="text-sm text-gray-500">TEXTO 03</p>
    </main>

    <!-- Footer fixo -->
    <footer class="w-full bg-gray-300 py-4 fixed bottom-0">
      <div class="flex justify-center space-x-4 px-6 max-w-6xl mx-auto">
        <!-- Cards do Footer -->
        <div
          v-for="(card, index) in cards"
          :key="index"
          class="flex-shrink-0 w-28 bg-white rounded-lg p-4 shadow-sm text-center"
        >
          <!-- Círculo da Imagem -->
          <div class="w-12 h-12 bg-gray-300 rounded-full mx-auto mb-2"></div>
          <p class="text-xs font-semibold text-gray-800">{{ card.name }}</p>
          <p class="text-xs text-gray-500">{{ card.date }}</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Dados dos cards
      cards: [
        { name: "NOME PESSOA 1", date: "01/01/1990" },
        { name: "NOME PESSOA 2", date: "02/02/1991" },
        { name: "NOME PESSOA 3", date: "03/03/1992" },
        { name: "NOME PESSOA 4", date: "04/04/1993" },
        { name: "NOME PESSOA 5", date: "05/05/1994" },
      ],
    };
  },
};
</script>

<style>
/* Importando a fonte Poppins */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap');

/* Configuração global */
body {
  font-family: 'Poppins', sans-serif;
  margin: 0;
}

.font-poppins {
  font-family: 'Poppins', sans-serif;
}

/* Footer fixo */
footer {
  background-color: #DCDCDC;
}
</style>
