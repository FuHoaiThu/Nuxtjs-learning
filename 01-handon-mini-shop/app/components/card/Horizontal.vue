<template>
  <section class="card" v-if="card">
    <div class="card-image" role="img" :aria-label="card.title">
      {{ card.icon }}
    </div>
    <div class="card-content">
      <p class="card-content__eyebrow">Product #{{ card.id }}</p>
      <h2>{{ card.title }}</h2>
      <p class="card-content__muted">{{ card.description }}</p>
      <p class="card-content__price">{{ card.price }}</p>
      <p class="card-content__muted">Available now · Free standard shipping</p>
      <button>
        <router-link to="/products">← Back to products</router-link>
      </button>
    </div>
  </section>
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
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 35px;
  padding: 32px;
  margin: 15px 0 70px;
  background-color: var(--color-white);
  border: 1px solid var(--color-grey-1);
  border-radius: 15px;
  overflow: hidden;
  .card-image {
    min-height: 300px;
    border-radius: 14px;
    place-items: center;
    display: grid;
    font-size: 120px;
    background: linear-gradient(140deg, #eef3ff, #e9f6f6);
  }
  .card-content {
    .card-content__eyebrow {
      color: var(--color-blue-1);
      font-size: 13px;
      font-weight: bold;
      letter-spacing: 1.3;
      text-transform: uppercase;
      margin: 0;
    }
    h2 {
      margin-top: 0;
    }
    .card-content__muted {
      color: var(--color-blue-4);
    }
    .card-content__price {
      font-size: 20px;
      font-weight: bold;
      margin: 14px 0 20px;
    }
    button {
      border: none;
      outline: none;
      border-radius: 9px;
      cursor: pointer;
      a {
        font-weight: bold;
        text-decoration: none;
        font-size: 14px;
        color: var(--color-blue-5);
        padding: 12px 20px;
        background-color: var(--color-grey-blue-3);
      }
    }
  }
}
</style>
