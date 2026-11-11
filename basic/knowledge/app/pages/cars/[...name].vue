<template><h1>Cars page</h1><p>Params: {{ params }}</p></template>
<script setup>
const route = useRoute()
const params = route.params.name
</script>