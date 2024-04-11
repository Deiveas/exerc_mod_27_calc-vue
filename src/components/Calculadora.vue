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

<template>
    <div class="rounded bg-danger pt-4 pb-4">
      <numero-input class="space bg-danger m-1" label="Número 1:" @numeroAtualizado="atualizarNumero1"></numero-input>
      <numero-input class="space bg-danger m-4" label="Número 2:" @numeroAtualizado="atualizarNumero2"></numero-input>
      <operacao-select class="space bg-danger m-4" label="Operação:" @operacaoAtualizada="atualizarOperacao"></operacao-select>
      <div class="bg-danger">
        <h2>Resultado: {{ resultado }}</h2>
      </div>
    </div>
  </template>
  