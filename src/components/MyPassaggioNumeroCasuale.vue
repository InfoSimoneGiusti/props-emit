<template>
  <button @click="$emit('eventoNumeroCasuale', generaEventoNumeroCasuale())">Genera un numero a caso!</button>
</template>

<script>
export default {
    name: "MyPassaggioNumeroCasuale",
    methods: {
        generaEventoNumeroCasuale() {
            return Math.floor(Math.random() * 10);
        }
    }
}
</script>

<style>

</style>