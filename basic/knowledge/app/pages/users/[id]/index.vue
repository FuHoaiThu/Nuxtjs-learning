<template><h1>User by ID: {{ id }}</h1></template>
<script setup>
const route = useRoute();
const id = computed(() => {
  return route.params.id || "none";
});
</script>
