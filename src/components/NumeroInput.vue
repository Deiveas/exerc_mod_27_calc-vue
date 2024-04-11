<script>
export default {
  props: ["label"],
  data() {
    return {
      numero: 0,
    };
  },
  methods: {
    atualizarNumero() {
      this.$emit("numeroAtualizado", this.numero);
    },
  },
};
</script>

<template>
  <div>
    <label>{{ label }}</label>
    <input class="m-1" type="number" v-model="numero" @input="atualizarNumero" />
  </div>
</template>
