<template><h1>Contact</h1></template>

<script setup>
const title = ref("Contract");

setTimeout(() => {
  title.value = "New Contract";
}, 2000);
useHead({
  title,
});
</script>
