<script>
export default {
  data() {
    return {
      moedas: [
        { moeda: "USD", nome: "Dolar americano" },
        { moeda: "EUR", nome: "Euro" },
        { moeda: "£", nome: "Libra Esterlina" },
        { moeda: "JPY", nome: "Lene" },
        { moeda: "AUD", nome: "Dolar Australiano" },
        { moeda: "CHF", nome: "Franco Suiço" },
        { moeda: "CAD", nome: "Dolar Canadense" },
        { moeda: "CNY", nome: "Renminbi(Yuan)"},
        { moeda: "ARS", nome: "Peso Argentino"},
        { moeda: "YTL", nome: "Lira Turca"},
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="linhaCima"></div>
    <img src="@/assets/img/denverlacasadepapel.jpg" alt="" />
    <h1>Conversor de Moedas</h1>
    <p>
      Dolar americano, Euro, Libra Estelina, Lene, Dolar Australiano, Franco
      Suiço, Dolar Canadense, Renminbi(yuan), Peso argentino, Lira Turca
    </p>
    <div class="linhaBaixo"></div>
  </header>

  <main>
    <div class="fundo">
      <label for="valor">Valor:</label>
      <input id="valor" placeholder="1,00" type="number" />
      <label for="conversão">Converter de:</label>
      <select name="unidades" id="conversão">
        <option
          v-for="moeda of moedas"
          :key="moeda.moeda"
          for="conversão"
          value="moeda.moeda"
        >
          {{ moeda.nome }}
        </option>
      </select>
      <p>=</p>
      <input type="text" />
      Para:
      <!-- /button// -->
      <input type="number" />
      Resultado da conversão
      <!-- /button// -->
    </div>
  </main>
</template>

<style>
@import "./assets/style.css";
</style>
