<template>
  <div>
    <header class="header">
      <a class="logo" href="/">Mini Shop <span class="logo-dot">.</span></a>
    </header>
    <slot />
  </div>
</template>
<style lang="css" scoped>
header {
  width: 82%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  .logo {
    text-decoration: none;
    cursor: pointer;
  }
}
</style>
