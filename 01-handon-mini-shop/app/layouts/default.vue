<template>
  <div>
    <header class="header">
      <div class="header-wrapper">
        <a class="logo" href="/">Mini Shop<span class="logo-dot">.</span></a>
        <nav>
          <ul>
            <li v-for="menu in menus" :key="menu.id">
              <nuxt-link :to="menu.url">{{ menu.title }}</nuxt-link>
            </li>
          </ul>
        </nav>
      </div>
    </header>
    <slot />
  </div>
</template>
<script setup>
const menus = [
  {
    id: 0,
    title: "Home",
    url: "/",
  },
  {
    id: 1,
    title: "Products",
    url: "/products",
  },
  {
    id: 0,
    title: "About",
    url: "about",
  },
  {
    id: 0,
    title: "Admin",
    url: "admin",
  },
];
</script>
<style lang="css" scoped>
.header {
  border-bottom: 1px solid var(--color-grey-1);
  background-color: var(--color-white);
}
.header-wrapper {
  width: 82%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-height: 76px;
  .logo {
    text-decoration: none;
    cursor: pointer;
    font-weight: bold;
    font-size: 23px;
    letter-spacing: -0.8px;
    .logo-dot {
      color: var(--color-blue-1);
    }
  }
  nav {
    ul {
      display: flex;
      align-items: center;
      gap: 25px;
    }
    ul li {
      list-style-type: none;
      a {
        text-decoration: none;
        font-size: 14px;
        color: var(--color-dark-blue-2);
      }
      .router-link-exact-active {
        font-weight: bold;
        color: var(--color-blue-2);
      }
    }
  }
}
</style>
