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

<template>
    <div>
      <label>{{ label }}</label>
      <select class="m-1" v-model="operacao" @change="atualizarOperacao">
        <option value="+">Adição</option>
        <option value="-">Subtração</option>
        <option value="*">Multiplicação</option>
        <option value="/">Divisão</option>
      </select>
    </div>
  </template>

  