<template>
  <article class="card">
    <div class="product-image" role="img" aria-label="Wireless Headphones">
      {{ card.icon }}
    </div>
    <div class="card-body">
      <h2>{{ card.title }}</h2>
    </div>
  </article>
</template>
<script setup>
const props = defineProps({
  card: {
    type: Object,
    defaut: () => {},
  },
});
</script>
<style lang="css" scoped>
.card {
  background-color: var(--color-white);
  border: 1px solid var(--color-grey-1);
  border-radius: 15px;
  .product-image {
    height: 210px;
    display: grid;
    place-items: center;
    font-size: 80px;
    background: linear-gradient(140deg, #eef3ff, #e9f6f6);
  }
  .card-body {
    background-color: var(--color-white);
    padding: 22px;
    h2 {
      font-size: 22px;
      margin: 0 0 8px;
    }
  }
}
</style>
