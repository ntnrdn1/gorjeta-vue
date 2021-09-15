<template>
  <div id="container">
    <form @submit.prevent="calcular">
      <div>
        <label>Valor da conta</label>
      </div>
      <input v-model.number="valorConta" />

      <div>
        <label>% de Gorjeta</label>
        <div id="porcentagem"><input v-model.number="porcentagem" /><span>%</span></div>
        <small>O Valor padrão é 10%</small>
      </div>

      <button type="submit">calcular</button>
    </form>
    <p>Valor da gorjeta: {{ gorjeta }}</p>
    <p>Valor total: {{ valorTotal }}</p>
  </div>
</template>

<script lang="ts">

import { defineComponent } from 'vue';

export default defineComponent({
  name: "App",
  data() {
    return {
      valorConta: 0,
      porcentagem: 10,
      valorTotal: 0,
      gorjeta: 0,
    };
  },
  methods: {
    calcular() {
      const { valorConta, porcentagem } = this;
      this.gorjeta = (valorConta * porcentagem) / 100;
      const { gorjeta } = this;
      this.valorTotal = gorjeta + valorConta;
    },
  },
});
</script>

<style scoped>
#container {
  text-align: center;
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  color: #8c8c8c;
  margin: 0;
}

#container a {
  text-decoration: none;
}

button {
  margin: 1%;
}

#porcentagem {
  margin-bottom: 5px;
}

</style>