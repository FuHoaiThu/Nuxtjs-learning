<template>
  <h1>Contact</h1>
  <button @click="setPageLayout('default')">Change Layout</button>
</template>

<script setup>
definePageMeta({
  layout: "secondary",
});
</script>
