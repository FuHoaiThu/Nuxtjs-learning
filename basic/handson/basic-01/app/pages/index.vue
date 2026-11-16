<template>
  <section class="hero">
    <div>
      <span class="eyebrow">NUXT 4 · ROUTING HANDS-ON</span>
      <h1>Discover your next<br /><em>favorite setup.</em></h1>
      <p>
        Explore thoughtfully selected essentials for a workspace that feels like
        yours.
      </p>
      <button><a>Explore products →</a></button>
    </div>
    <div class="hero-art" aria-hidden="true">
      <div></div>
      <div></div>
    </div>
  </section>
</template>
<style lang="css" scoped>
.hero {
  min-height: 450px;
  background-color: #eae8ff;
  border-radius: 24px;
  padding: 55px 70px;
  display: grid;
  grid-template-columns: 1.1fr 1fr;
  .eyebrow {
    font-size: 11px;
    font-weight: 800;
    letter-spacing: 2.1px;
    color: #6554d9;
  }
  h1 {
    font:
      800 clamp(40px, 5vw, 64px) / 1.07 Outfit,
      sans-serif;
    letter-spacing: -2px;
    margin: 20px 0;
  }
  em {
    font-style: normal;
    color: #6554d9;
  }
  p {
    max-width: 390px;
    color: #66708a;
    line-height: 1.8;
    font-size: 15px;
    margin: 1em 0;
  }
}
</style>
