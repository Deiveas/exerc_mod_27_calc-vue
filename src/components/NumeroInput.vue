<template>
    <div>
      <label>{{ label }}</label>
      <input type="number" v-model="numero" @input="atualizarNumero" />
    </div>
  </template>
  
  <script>
  export default {
    props: ['label'],
    data() {
      return {
        numero: 0
      };
    },
    methods: {
      atualizarNumero() {
        this.$emit('numeroAtualizado', this.numero);
      }
    }
  };
  </script>
  
  <style scoped>
  /* Estilos opcionais */
  </style>
  