<template>
  <article class="card">
    <div class="product-image" role="img" :aria-label="card.title">
      {{ card.icon }}
    </div>
    <div class="card-body">
      <h2>{{ card.title }}</h2>
      <p class="card-body__des">{{ card.description }}</p>
      <p class="card-body__price">{{ card.price }}</p>
      <button><router-link :to="`products/${card.id}`">View Details →</router-link></button>
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
    .card-body__des {
      color: var(--color-blue-4);
      line-height: 1.6;
    }
    .card-body__price {
      font-size: 20px;
      font-weight: bold;
      margin: 14px 0 20px;
    }
    button {
      border: none;
      outline: none;
      border-radius: 9px;
      background-color: var(--color-dark-blue-3);
      padding: 12px 20px;
      cursor: pointer;
      a {
        text-decoration: none;
        font-weight: bold;
        font-size: 14px;
        color: var(--color-white);
      }
    }
  }
}
</style>
