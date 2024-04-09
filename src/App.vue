<template>
    <div id="app">
      <header>
        <h1>Calculadora Vue.js</h1>
      </header>
      <main>
        <Calculadora />
      </main>
    </div>
  </template>
  
  <script>
  import Calculadora from './components/Calculadora.vue';
  
  export default {
    components: {
      Calculadora
    }
  };
  </script>
  
  <style>
  /* Adicione estilos conforme necessário */
  </style>
  
