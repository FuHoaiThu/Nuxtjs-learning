<template>
  <main>
    <section class="wrapper">
      <Hero :content="heroContent" />
      <Panel />
      <section>
        <h2>Featured products</h2>
        <Products />
      </section>
    </section>
  </main>
</template>
<script setup>
const heroContent = {
  eyebrow: "Welcome to Mini Shop",
  header: "Find your everyday favorites.",
  lead: "Simple, useful products chosen to make your day better. Explore our small collection and find something you love.",
};
</script>
