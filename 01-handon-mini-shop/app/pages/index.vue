<template>
  <main>
    <section class="wrapper">
      <section class="hero">
        <p class="hero-eyebrow">Welcome to Mini Shop</p>
        <h1>Find your everyday favorites.</h1>
        <p class="hero-lead">
          Simple, useful products chosen to make your day better. Explore our
          small collection and find something you love.
        </p>
      </section>
      <Panel />
      <section>
        <h2>Featured products</h2>
        <ul class="products">
          <li v-for="card in products" :key="card.id">
            <Card :card="card" />
          </li>
        </ul>
      </section>
    </section>
  </main>
</template>
<script setup>
const products = [
  {
    id: 0,
    title: "Wireless Headphones",
    descrition: "Clear sound, comfortable fit, and all-day listening.",
    price: "$129",
    icon: "🎧",
  },
  {
    id: 1,
    title: "Smart Watch",
    descrition: "Track your day with a sleek, everyday smart watch.",
    price: "$199",
    icon: "⌚",
  },
  {
    id: 2,
    title: "Running Shoes",
    descrition: "Lightweight shoes designed for daily movement.",
    price: "$89",
    icon: "👟",
  },
];
</script>
<style lang="css" scoped>
main {
  .wrapper {
    width: 82%;
    margin: 0 auto;
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
  }
}
</style>
