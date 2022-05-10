<script>
export default {
    name: "mainPrincipal",
    data() {
    return {
      moedas: [
        { moeda: "USD", nome: "Dolar americano" },
        { moeda: "EUR", nome: "Euro" },
        { moeda: "GBP", nome: "Libra Esterlina" },
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
        <p id="igual">=</p>
        <input type="text" />
        Para:
        <!-- /button// -->
        <input type="number" />
        Resultado da conversão
        <!-- /button// -->
      </div>
  </main>
</template>