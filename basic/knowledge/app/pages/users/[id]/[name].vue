<template>
  <h1>User by id and name</h1>
  <p>ID: {{ id }}</p>
  <p>Name: {{ name }}</p>
</template>
<script setup>
const route = useRoute();
const id = computed(() => route.params.id);
const name = computed(() => route.params.name);
</script>
