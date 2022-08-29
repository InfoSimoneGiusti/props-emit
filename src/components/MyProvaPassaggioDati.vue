<template>
  <button @click="$emit('provaPassaggioDati', 'Il valore che voglio passare', 'secondo valore')">Prova a passare un valore</button>
</template>

<script>
export default {
    name: 'MyProvaPassaggioDati'
}
</script>

<style>

</style>