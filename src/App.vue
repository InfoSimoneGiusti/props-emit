<template>
  <div id="app">
    <MyContatore :numeroDiClick="numeroDiClick" />

    <MyBottone @pincopallino="incrementaDiUno" />

    <MyProvaPassaggioDati @provaPassaggioDati="ricevoDatiDaFiglio"/>

    <!-- <button @click="incrementaDiUno">Incrementa contatore</button> -->


    <h2>Numero casuale: {{numeroCasuale}}</h2>
    <MyPassaggioNumeroCasuale @eventoNumeroCasuale="ricevoNumeroCasuale" />

  </div>
</template>

<script>
import MyContatore from './components/MyContatore.vue';
import MyBottone from './components/MyBottone.vue';
import MyProvaPassaggioDati from './components/MyProvaPassaggioDati.vue';
import MyPassaggioNumeroCasuale from './components/MyPassaggioNumeroCasuale.vue';

export default {
  name: 'App',
  components: {
    MyContatore,
    MyBottone,
    MyProvaPassaggioDati,
    MyPassaggioNumeroCasuale
  },
  data() {
    return {
      numeroDiClick: 10,
      numeroCasuale: 0,
    }
  },
  methods: {
    incrementaDiUno() {
      this.numeroDiClick ++;
    },
    ricevoDatiDaFiglio(datoCheVoglioRicevere, secondoValoreRicevuto) {
      alert(secondoValoreRicevuto)
    },
    ricevoNumeroCasuale(numeroCasualeRicevuto) {
      this.numeroCasuale = numeroCasualeRicevuto;
    }
  }
}
</script>

<style lang="scss">

</style>
