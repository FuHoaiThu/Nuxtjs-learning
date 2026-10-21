<template>
  <section class="hero">
    <p class="hero-eyebrow">{{ content.eyebrow }}</p>
    <h1>{{ content.header }}</h1>
    <p class="hero-lead">
      {{ content.lead }}
    </p>
  </section>
</template>
<script setup>
const props = defineProps({
  content: {
    type: Object,
    default: () => {
      eyebrow: "";
      header: "";
      lead: "";
    },
  },
});
</script>
<style lang="css" scoped>
.hero {
  padding: 70px 0 34px;
  .hero-eyebrow {
    color: var(--color-blue-1);
    font-size: 13px;
    font-weight: bold;
    letter-spacing: 1.3px;
    text-transform: uppercase;
  }
  h1 {
    font-size: clamp(30px, 5vw, 49px);
    margin: 12px 0;
  }
  .hero-lead {
    max-width: 640px;
    font-size: 17px;
    line-height: 1.7;
    color: var(--color-blue-3);
  }
}
</style>
