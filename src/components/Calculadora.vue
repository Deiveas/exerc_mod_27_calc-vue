<template>
    <div>
      <numero-input label="Número 1" @numeroAtualizado="atualizarNumero1"></numero-input>
      <numero-input label="Número 2" @numeroAtualizado="atualizarNumero2"></numero-input>
      <operacao-select label="Operação" @operacaoAtualizada="atualizarOperacao"></operacao-select>
      <div>
        <h2>Resultado: {{ resultado }}</h2>
      </div>
    </div>
  </template>
  
  <script>
  import NumeroInput from './NumeroInput.vue';
  import OperacaoSelect from './OperacaoSelect.vue';
  
  export default {
    components: {
      NumeroInput,
      OperacaoSelect
    },
    data() {
      return {
        numero1: 0,
        numero2: 0,
        operacao: '+',
        resultado: 0
      };
    },
    methods: {
      atualizarNumero1(valor) {
        this.numero1 = valor;
        this.calcular();
      },
      atualizarNumero2(valor) {
        this.numero2 = valor;
        this.calcular();
      },
      atualizarOperacao(operacao) {
        this.operacao = operacao;
        this.calcular();
      },
      calcular() {
        switch (this.operacao) {
          case '+':
            this.resultado = this.numero1 + this.numero2;
            break;
          case '-':
            this.resultado = this.numero1 - this.numero2;
            break;
          case '*':
            this.resultado = this.numero1 * this.numero2;
            break;
          case '/':
            this.resultado = this.numero1 / this.numero2;
            break;
          default:
            this.resultado = 0;
        }
      }
    }
  };
  </script>
  
  <style scoped>
  /* Estilos opcionais */
  </style>
  