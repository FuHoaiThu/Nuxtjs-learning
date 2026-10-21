<template>
  <ul class="products">
    <li v-for="card in products" :key="card.id">
      <CardVertical :card="card" />
    </li>
  </ul>
</template>
<script setup>
import { products } from "~/data";
</script>
<style lang="css" scoped>
.products {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 22px;
  padding-bottom: 65px;
  padding-left: 0;
  li {
    list-style-type: none;
  }
}
</style>
