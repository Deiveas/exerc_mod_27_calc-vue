<script>
  import Calculadora from './components/Calculadora.vue';
  
  export default {
    components: {
      Calculadora
    }
  };
  </script>

<template>
    <div id="app" class="container text-center mt-5 pb-5">
      <header>
        <h1 class>Calculadora Vue.js</h1>
      </header>
      <main>
        <Calculadora />
      </main>
    </div>
  </template>
  
  <style>
  html, div {
    background-color: red;
    color: white;
  }
  </style>
  
