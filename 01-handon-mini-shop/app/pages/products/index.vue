<template>
  <section class="wrapper">
    <Hero :content="heroContent" />
    <Products />
  </section>
</template>
<script setup>
const heroContent = {
  eyebrow: "Our collection",
  header: "Our Products",
  lead: "Discover our carefully selected products.",
};
</script>
