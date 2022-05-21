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
    <div class="container" id="conversao">
      <div class="inputValor">
        <label for="valor">Valor:</label>
        <input id="valor" placeholder="1,00" type="number" />
      </div>
      <div class="inputConversaoDe">
        <label for="conversaoDe">Converter de:</label>
        <select name="unidades" id="conversaoDe">
          <option
            v-for="moeda of moedas"
            :key="moeda.moeda"
            for="conversão"
            value="moeda.moeda"
          >
            {{ moeda.nome }}
          </option>
        </select>
      </div>
      <div class="igual">=</div>
      <div class="inputConversaoPara">
        <label for="conversaoPara">Para:</label>
        <select name="unidades" id="conversaoPara">
          <option
            v-for="moeda of moedas"
            :key="moeda.moeda"
            for="conversão"
            value="moeda.moeda"
          >
            {{ moeda.nome }}
          </option>
        </select>            
      </div>
      <br>
    </div>
    <div class="resultado">
      <label class="resultadoC" for="resultadoDaConversao">Resultado da conversão:
        <input type="number" id="resultadoDaConversao"/>
      </label>
    </div>
  </main>
</template>