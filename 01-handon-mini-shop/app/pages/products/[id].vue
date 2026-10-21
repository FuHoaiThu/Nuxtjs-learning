<template>
  <section class="wrapper">
    <Hero :content="heroContent" />
    <CardHorizontal :card="productDetail" />
  </section>
</template>
<script setup>
import { products } from "~/data";

const route = useRoute();
const productId = computed(() => {
  return route.params.id;
});
const productDetail = computed(() => {
  return products.find((p) => p.id === Number(productId.value));
});

const heroContent = computed(() => {
  return {
    eyebrow: "Product detail",
    header: productDetail.value?.title || "",
    lead: productDetail.value?.description || "",
  };
});
</script>
