<template>
  <h1>Hai cliccato {{numeroDiClick}} volte</h1>
</template>

<script>
export default {
    name: 'MyContatore',
    props: {
        numeroDiClick: Number
    }
}
</script>

<style>

</style>