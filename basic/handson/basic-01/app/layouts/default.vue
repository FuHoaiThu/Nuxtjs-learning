<template>
  <div id="content">
    <header>
      <a class="brand" href="/">Onyra Yuki <span>❀</span></a>
      <nav aria-label="Main navigation">
        <ul>
          <li v-for="menu in menus" :key="menu.id">
            <a :class="{ active: menu.id === 1 }">{{ menu.label }}</a>
          </li>
        </ul>
      </nav>
    </header>
    <slot />
  </div>
</template>
<script setup>
const menus = [
  {
    id: 1,
    label: "Home",
  },
  {
    id: 2,
    label: "Experience",
  },
];
</script>
<style lang="css" scoped>
#content {
  background-color: #fff9f7ee;
  border-bottom: 1px solid #f1d9dd;
  position: sticky;
  top: 0;
  left: 0;
  header {
    padding: 10px 0;
    max-width: 82%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .brand {
      font-weight: 700;
      font-size: 30px;
      text-decoration: none;
      font-style: italic;
      color: #bd4b70;
      span {
        color: #879a76;
        font-size: 22px;
      }
    }
    nav {
      font-size: 14px;
      ul {
        display: flex;
        gap: 8px;
        flex-wrap: wrap;
        li {
          list-style-type: none;
          a {
            cursor: pointer;
            padding: 8px 18px;
            border-radius: 99px;
          }
          .active {
            background-color: #fbe0e7;
            color: #a73e61;
          }
        }
      }
    }
  }
}
</style>
