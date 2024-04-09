<template>
    <div>
      <label>{{ label }}</label>
      <select v-model="operacao" @change="atualizarOperacao">
        <option value="+">Adição</option>
        <option value="-">Subtração</option>
        <option value="*">Multiplicação</option>
        <option value="/">Divisão</option>
      </select>
    </div>
  </template>
  
  <script>
  export default {
    props: ['label'],
    data() {
      return {
        operacao: '+'
      };
    },
    methods: {
      atualizarOperacao() {
        this.$emit('operacaoAtualizada', this.operacao);
      }
    }
  };
  </script>
  
  <style scoped>
  /* Estilos opcionais */
  </style>
  