<template>
  <section class="panel">
    <h2>Discover our collection</h2>
    <p class="panel-muted">
      From headphones to running shoes, there is something for everyone.
    </p>
    <button><nuxt-link to="/products">Shop products →</nuxt-link></button>
  </section>
</template>
<style lang="css" scoped>
.panel {
  padding: 32px;
  margin: 15px 0 70px;
  background-color: var(--color-white);
  border: 1px solid var(--color-grey-1);
  border-radius: 15px;
  overflow: hidden;
  h2 {
    margin-top: 0;
  }
  .panel-muted {
    line-height: 1.6;
    color: var(--color-blue-4);
  }
  button {
    outline: none;
    border: none;
    border-radius: 9px;
    background-color: var(--color-dark-blue-3);
    padding: 12px 20px;
    cursor: pointer;
    a {
      color: var(--color-white);
      text-decoration: none;
      font-size: 14px;
      font-weight: bold;
    }
  }
}
</style>
