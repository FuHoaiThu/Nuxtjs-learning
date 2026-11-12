<template><h1>Contact</h1></template>
<script setup>
const title = ref("Contact Page");
setTimeout(() => {
  title.value = "New Contact";
}, 2000);
useHead({
  title,
});
</script>
